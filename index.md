
# Simulation of PTP (IEEE 1588)

**ptp-sim** is a community effort to provide a simulation framework for the Precision Time Protocol (PTP) as specified in [IEEE 1588-2008][1].
It is based on [OMNeT++][2] and the [INET Framework][3]. Discussions about ptp-sim happen at the [discussion forum](http://ptp-sim.boards.net).

<style>
video {
  max-width: 100%;
  height: auto;
}
img {
  max-width: 100%;
  height: auto;
}
</style>

<video src="img/banner/banner.webm" poster="img/banner/banner.png" autoplay loop preload>
</video>

[1]: https://standards.ieee.org/standard/1588-2008.html
[2]: https://omnetpp.org/
[3]: https://inet.omnetpp.org/

## Project overview

The ptp-sim project is the host for the following sub-projects:

* [OMNeT_Utils](https://github.com/ptp-sim/OMNeT_Utils)
* [libPTP](https://github.com/ptp-sim/libPTP)
* [PTP_Simulations](https://github.com/ptp-sim/PTP_Simulations)
* [libPLN](https://github.com/ptp-sim/libPLN)

The relationship between these projects and various other projects is sketched in the following image:

![Project relationship](img/project_relationships.png)

The core projects of ptp-sim are __libPTP__ and __libPLN__. __LibPTP__ provides different kinds of simulations models for OMNeT++ to simulate time synchronization as specified in IEEE 1588. This includes a PTP stack and simulation models of PTP-capable network cards. Time synchronization is necessary to counter the errors that affect real clocks. Thus, generation of time synchronization makes only sense if these clock errors are also simulated. __LibPLN__ provides realistic clock noise for our simulations, and does so efficiently (which is important for the simulation of larger networks).

The __PTP_Simulations__ project provides examples to show what can be done with libPTP and libPLN. It should serve as a starting point for new users, to help them create their own simulations.

__OMNeT_Utils__ is a collection of generic simulation models which have been developed to support libPTP.  These models are not specific to libPTP, and they could be useful for other OMNeT++ projects. They are kept in their own project to make the usage in other projects easily possible.

The ptp-sim projects make heavy use of other projects:
* INET framework: The INET framework provides many different simulation models of network components for OMNeT++.
* Boost C++ library: We use several algorithm implementations from the Boost library.
* FFTW: The Fastest Fourier Transform in the West. It's a Fourier Transform. And it's fast. We use if for the filter implementation in our clock noise generation.
* Spline: A cubic spline interpolation.

The ptp-sim projects would not be possible without these other open source projects. __Thank you!__


## Further information

* [Install Guide](Install_Guide)
* [Usage Examples](Usage Examples)
* [Current State](Usage Examples)
* [Contribute](Contribute)
* [Release Planning](Release Planning)

## Contact

Please visit the [ptp-sim discussion forum](http://ptp-sim.boards.net) for further discussions.
