# model-radmc3d-v0.39
Generic protoplanetary disk model with a simple chemistry

The density is given by
            Sigma(r,phi)          /   z^2    \
    rho =  ---------------- * exp| - -------- |
            Hp * sqrt(2*pi)       \   2*Hp^2 /
    Sigma - surface density
    Hp    - Pressure scale height
    Hp/r  = hrdisk * (r/rdisk)^plh
The molecular abundance function takes into account dissociation and freeze-out of the molecules
For photodissociation only the continuum (dust) shielding is taken into account in a way that
whenever the continuum optical depth radially drops below a threshold value the molecular abundance
is dropped to zero. For freeze-out the molecular abundance below a threshold temperature is decreased
by a given fractor.

Function Documentation

def radmc3dPy.model ppdisk.getDefaultParams ( )
Function to provide default parameter values

def radmc3dPy.model ppdisk.getDustDensity ( rcyl = None, phi = None, z = None, z0 = None, hp = None, sigma=None, grid=None, ppar=None)
Function to create the density distribution in a protoplanetary disk


