---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMDSPDeviceControl::GetCapabilities


## -description



The <b>GetCapabilities</b> method retrieves the capabilities mask for the device with which this control interface is associated. The capabilities describe the methods of the device control that are supported by the media device.




## -parameters




### -param pdwCapabilitiesMask [out]

Pointer to a <b>DWORD</b> containing the capabilities of the device. The following flags can be returned in this variable.

<table>
<tr>
<th>
                  Flag
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>MDM_DEVICECAP_CANPLAY</td>
<td>The media device can play MP3 audio.</td>
</tr>
<tr>
<td>MDM_DEVICECAP_CANSTREAMPLAY</td>
<td>The media device can play streaming audio directly from the host computer.</td>
</tr>
<tr>
<td>MDM_DEVICECAP_CANRECORD</td>
<td>The media device can record audio.</td>
</tr>
<tr>
<td>MDM_DEVICECAP_CANSTREAMRECORD</td>
<td>The media device can record streaming audio directly to the host computer.</td>
</tr>
<tr>
<td>MDM_DEVICECAP_CANPAUSE</td>
<td>The media device can pause during play or record operations.</td>
</tr>
<tr>
<td>MDM_DEVICECAP_CANRESUME</td>
<td>The media device can resume an operation from a pause command.</td>
</tr>
<tr>
<td>MDM_DEVICECAP_CANSTOP</td>
<td>The media device can stop playing before the end of a file.</td>
</tr>
<tr>
<td>MDM_DEVICECAP_CANSEEK</td>
<td>The media device can seek to a position other than the beginning of a file.</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwCapabilitiesMask</i> parameter is an invalid or <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a196edef-f670-4c1f-92bd-172a75f3f420">IMDSPDeviceControl Interface</a>
 

 

