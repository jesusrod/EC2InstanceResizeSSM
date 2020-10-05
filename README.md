# EC2InstanceResizeSSM
EC2 Resize Instance and update AWS PV Drivers

Copyright (c) 2020. Amazon Web Services Ireland LTD. All Rights Reserved. AWS Enterprise Support Team Name : AutoStopCW-Lambda Version : 1.0.0 Encoded : No Paramaters : None Platform : Any EC2 Associated Files: None Abstract : ReadMe Document Revision History : - 1.0.0 | 07/05/2020 Initial Version Author : Jesus Rodriguez

##################### Automation Stop and Start.################################################ YOU ACKNOWLEDGE AND AGREE THAT THE SCRIPT IS PROVIDED FREE OF CHARGE "AS IS" AND "AVAILABLE" BASIS, AND THAT YOUR USE OF RELIANCE UPON THE APPLICATION OR ANY THIRD PARTY CONTENT AND SERVICES ACCESSED THEREBY IS AT YOUR SOLE RISK AND DISCRETION. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

################################################################################################ EC2 Resize Instance and update AWS PV Drivers

This Automation given the InstanceID will run the following steps:

* Get Root volumeID with the InstanceID provided
* CreateSnapshot - it will create a volume snapshot of the root volume and will capture the snapshot id.
* Verify Snapshot - it will wait until the snapshot is complete
* Install AWS ENA Network Driver
* Install AWS NVMe
* Install AWS PVDriver
* Stop EC2 Instance
* Enable ENA Support once Instance is in "Stopped" state
* Resize EC2 instance
* Start EC2 Instance

This Automation requires the EC2 Instance to have Internet Access as it needs to download drivers
