---
UID: NF:strmif.IAMExtDevice.GetCapability
title: IAMExtDevice::GetCapability
author: windows-driver-content
description: The GetCapability method retrieves the capabilities of the external device.
old-location: dshow\iamextdevice_getcapability.htm
old-project: DirectShow
ms.assetid: 4efed2b8-a62c-4a82-bc2d-c6d3a202263c
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: GetCapability, GetCapability method [DirectShow], GetCapability method [DirectShow],IAMExtDevice interface, IAMExtDevice interface [DirectShow],GetCapability method, IAMExtDevice.GetCapability, IAMExtDevice::GetCapability, IAMExtDeviceGetCapability, dshow.iamextdevice_getcapability, strmif/IAMExtDevice::GetCapability
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMExtDevice.GetCapability
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMExtDevice::GetCapability


## -description



The <code>GetCapability</code> method retrieves the capabilities of the external device.




## -parameters




### -param Capability [in]

Specifies the capability to check. See Remarks for more information.


### -param pValue [out]

Pointer to a variable that receives a <b>long</b> integer. See Remarks for more information.


### -param pdblValue [out]

Pointer to a variable that receives a <b>double</b>. See Remarks for more information.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



The <i>Capability</i> parameter is a flag that specifies which capability to check. The method returns the result either in the <i>pValue</i> parameter or in the <i>pdblValue</i> parameter, depending on the capability flag.

For the following flags, the method returns the value OATRUE or OAFALSE in the <i>pValue</i> parameter. The value OATRUE indicates that the capability is present, while the value OAFALSE indicates it is absent.

<table>
<tr>
<th>
              Capability flag
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td>ED_DEVCAP_AUDIO_INPUTS</td>
<td>Device accepts audio input.</td>
</tr>
<tr>
<td>ED_DEVCAP_CAN_MONITOR_SOURCES</td>
<td>Device can send any input to the monitored output, regardless of the input that is currently selected.</td>
</tr>
<tr>
<td>ED_DEVCAP_CAN_PREVIEW</td>
<td>Device can preview.</td>
</tr>
<tr>
<td>ED_DEVCAP_CAN_RECORD</td>
<td>Device can record.</td>
</tr>
<tr>
<td>ED_DEVCAP_CAN_RECORD_STROBE</td>
<td>Device can strobe record. This capability applies to multitrack devices that can record to selected tracks.</td>
</tr>
<tr>
<td>ED_DEVCAP_CAN_SAVE</td>
<td>Device can save data.</td>
</tr>
<tr>
<td>ED_DEVCAP_CTLTRK_READ</td>
<td>Device can read control tracks.</td>
</tr>
<tr>
<td>ED_DEVCAP_HAS_AUDIO</td>
<td>Device has audio.</td>
</tr>
<tr>
<td>ED_DEVCAP_HAS_VIDEO</td>
<td>Device has video.</td>
</tr>
<tr>
<td>ED_DEVCAP_INDEX_READ</td>
<td>Device can read index marks.</td>
</tr>
<tr>
<td>ED_DEVCAP_NEEDS_CALIBRATING</td>
<td>Device needs calibrating. See <a href="https://msdn.microsoft.com/0c760669-c494-45bb-994e-5b4599db7de4">IAMExtDevice::Calibrate</a>.</td>
</tr>
<tr>
<td>ED_DEVCAP_TIMECODE_READ</td>
<td>Device can read SMPTE time code.</td>
</tr>
<tr>
<td>ED_DEVCAP_TIMECODE_WRITE</td>
<td>Device can set SMPTE time code.</td>
</tr>
<tr>
<td>ED_DEVCAP_USES_FILES</td>
<td>Device has a built-in file system.</td>
</tr>
<tr>
<td>ED_DEVCAP_VIDEO_INPUTS</td>
<td>Device accepts video input.</td>
</tr>
</table>
 

For the following flags, the method returns a defined constant in the <i>pValue</i> parameter.

ED_DEVCAP_DEVICE_TYPE: Returns the device type.

<table>
<tr>
<th>
              Returned Constant
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td>ED_DEVTYPE_ATR</td>
<td>Audio tape recorder</td>
</tr>
<tr>
<td>ED_DEVTYPE_CG</td>
<td>Character generator</td>
</tr>
<tr>
<td>ED_DEVTYPE_DDR</td>
<td>Digital disk recorder</td>
</tr>
<tr>
<td>ED_DEVTYPE_DVE</td>
<td>Digital video effects unit</td>
</tr>
<tr>
<td>ED_DEVTYPE_GPI</td>
<td>General purpose interface trigger</td>
</tr>
<tr>
<td>ED_DEVTYPE_KEYER</td>
<td>Video keyer</td>
</tr>
<tr>
<td>ED_DEVTYPE_LASERDISK</td>
<td>Laserdisc</td>
</tr>
<tr>
<td>ED_DEVTYPE_MIXER_AUDIO</td>
<td>Audio mixer</td>
</tr>
<tr>
<td>ED_DEVTYPE_MIXER_VIDEO</td>
<td>Video mixer</td>
</tr>
<tr>
<td>ED_DEVTYPE_ROUTER</td>
<td>Video router</td>
</tr>
<tr>
<td>ED_DEVTYPE_TBC</td>
<td>Timebase corrector</td>
</tr>
<tr>
<td>ED_DEVTYPE_TCG</td>
<td>Timecode generator/reader</td>
</tr>
<tr>
<td>ED_DEVTYPE_VCR</td>
<td>VCR, or camcorder with full VCR capabilities</td>
</tr>
<tr>
<td>ED_DEVTYPE_WIPEGEN</td>
<td>Video wipe generator</td>
</tr>
<tr>
<td>ED_DEVTYPE_JOYSTICK</td>
<td>Joystick</td>
</tr>
<tr>
<td>ED_DEVTYPE_KEYBOARD</td>
<td>Keyboard</td>
</tr>
</table>
 

ED_DEVCAP_SYNC_ACCURACY: Returns an indication of the device's synchronization accuracy.

<table>
<tr>
<th>
              Returned Constant
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td>ED_SYNCACC_PRECISE</td>
<td>Device has precise accuracy.</td>
</tr>
<tr>
<td>ED_SYNCACC_FRAME</td>
<td>Device is frame accurate.</td>
</tr>
<tr>
<td>ED_SYNCACC_ROUGH</td>
<td>Device is less than frame accurate.</td>
</tr>
</table>
 

ED_DEVCAP_NORMAL_RATE: Returns the device's normal frame rate.

<table>
<tr>
<th>
              Returned Constant
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td>ED_RATE_24</td>
<td>24 frames per second (fps)</td>
</tr>
<tr>
<td>ED_RATE_25</td>
<td>25 fps</td>
</tr>
<tr>
<td>ED_RATE_2997</td>
<td>29.97 fps</td>
</tr>
<tr>
<td>ED_RATE_30</td>
<td>30 fps</td>
</tr>
</table>
 

ED_DEVCAP_SEEK_TYPE: Returns an indication of the device's seeking accuracy.

<table>
<tr>
<th>
              Returned Constant
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td>ED_SEEK_PERFECT</td>
<td>Device can seek within one video frame without a signal break.</td>
</tr>
<tr>
<td>ED_SEEK_FAST</td>
<td>Device can seek quickly, with a short break in the signal.</td>
</tr>
<tr>
<td>ED_SEEK_SLOW</td>
<td>Device seeks slowly; such as tape transport.</td>
</tr>
</table>
 

For the following flags, the method returns a numeric value in the <i>pValue</i> parameter.

<table>
<tr>
<td>
              Capability Flag
            </td>
<td>
              Returned Value
            </td>
</tr>
<tr>
<td>ED_DEVCAP_EXTERNAL_DEVICE_ID</td>
<td>Manufacturer-specific identifier.</td>
</tr>
<tr>
<td>ED_DEVCAP_PREROLL</td>
<td>Device preroll time.</td>
</tr>
<tr>
<td>ED_DEVCAP_POSTROLL</td>
<td>Device postroll time.</td>
</tr>
</table>
 

In Windows XP Service Pack 2 and later, the following additional flags are supported for ED_DEVCAP_DEVICE_TYPE.

<table>
<tr>
<th>Returned Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_DEVTYPE_CAMERA_STORAGE</td>
<td>Storage for still images or short video files.</td>
</tr>
<tr>
<td>ED_DEVTYPE_DTV</td>
<td>Digital television with serial bus interface.</td>
</tr>
<tr>
<td>ED_DEVTYPE_PC_VIRTUAL</td>
<td>Virtual or emulated device on a computer.</td>
</tr>
</table>
 

To use these constants, include the header file Xprtdefs.h.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>
The <a href="https://msdn.microsoft.com/146ca753-fe41-49d3-8b1c-077e10a28192">MSDV</a> and UVC drivers support the following behaviors.

The ED_DEVCAP_NORMAL_RATE flag returns the frame rate.

<table>
<tr>
<th>Returned Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_RATE_25</td>
<td>25 fps (default PAL frame rate)</td>
</tr>
<tr>
<td>ED_RATE_2997</td>
<td>29.997 fps (default NTSC frame rate)</td>
</tr>
</table>
 

For MSDV only, the ED_DEVCAP_DEVICE_TYPE flag returns the device type. Possible values are shown in the following table.  For UVC devices, use the <a href="https://msdn.microsoft.com/641a10fe-8e8c-4225-b05e-b09dfb5f2fee">IKsTopologyInfo</a> interface instead.

<table>
<tr>
<th>Returned Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_DEVTYPE_CAMERA</td>
<td>Simple camera that can record or pause-record, but lacks full VCR capabilities.</td>
</tr>
<tr>
<td>ED_DEVTYPE_DVHS</td>
<td>Device supports D-VHS format.</td>
</tr>
<tr>
<td>ED_DEVTYPE_UNKNOWN</td>
<td>Unknown device type.</td>
</tr>
<tr>
<td>ED_DEVTYPE_VCR</td>
<td>Device has full VCR capabilities.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0423e888-39d1-45cb-9bcf-722240a31fbd">IAMExtDevice Interface</a>
 

 

