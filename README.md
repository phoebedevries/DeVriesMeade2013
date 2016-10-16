
The file channel_velocity.m containts a matlab function implementing the complete solution for an infinite solution of earthquakes. Input arguments and outputs are explained, and an example is provided, both here and at the beginning of the code:

The function ChannelVelocity calculates the velocity at points x at time t from the 3-layer viscoelastic earthquake cycle model. 

vfinal = ChannelVelocity(xfinal, slipRate, t, h, D, H, mu, eta, T)

Arguments:
   xfinal      : x values at which to evaluate solution, must be within 500 km of the fault
   slipRate    : slip rate [m/yr]
   t           : time since last earthquake [years]
   H           : thickness of elastic upper crust [km]
   D           : locking depth of the fault [km]
   h           : channel thickness of viscoelastic layer [km]
   mu          : shear modulus [Pa]
   eta         : dynamic viscocity [Pa s]
   T           : length of earthquake cycle [yrs]

 Returned variables:
   v           : velocity [mm/yr]
 
 Example:
 xfinal = linspace(-500, 500, 1000);
 vfinal = ChannelVelocity(xfinal, 1, 10, 20, 20, 20, 3e10, 1e18, 100);
 plot(xfinal, vfinal);


Reference: DeVries. P.R. and B.J. Meade, Earthquake cycle deformation in the Tibetan plateau with a weak mid-crustal layer, J. Geophys. Res., 118, 3101-3111.
