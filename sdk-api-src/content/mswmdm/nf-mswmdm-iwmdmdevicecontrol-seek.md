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

# IWMDMDeviceControl::Seek


## -description



The <b>Seek</b> method seeks to a position that is used as the starting point by the <a href="https://msdn.microsoft.com/e8d717e6-365c-44ad-b24e-daa3c35664de">Play</a> or <a href="https://msdn.microsoft.com/a9372ce9-e339-4664-9e12-4feae29529dc">Record</a> methods.




## -parameters




### -param fuMode [in]

Mode for the seek operation being performed. The <i>fuMode</i> parameter must be one of the following modes.

<table>
<tr>
<th>
                  Mode
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>WMDM_SEEK_BEGIN</td>
<td>Seek to a position that is <i>nOffset</i> units after the beginning of the file.</td>
</tr>
<tr>
<td>WMDM_SEEK_CURRENT</td>
<td>Seek to a position that is <i>nOffset</i> units from the current position.</td>
</tr>
<tr>
<td>WMDM_SEEK_END</td>
<td>Seek to a position that is <i>nOffset</i> units before the end of the file.</td>
</tr>
<tr>
<td>WMDM_SEEK_REMOTECONTROL</td>
<td>Seek the removable control.</td>
</tr>
<tr>
<td>WMDM_SEEK_STREAMINGAUDIO</td>
<td>Seek the streaming audio.</td>
</tr>
</table>
 


### -param nOffset [in]

Number of units by which the seek operation moves the starting position away from the origin specified by <i>fuMode</i>. The units of <i>nOffset</i> are defined by the content. They can be milliseconds for music, pages for electronic books, and so on.

A positive value for <i>nOffset</i> indicates seeking forward through the file. A negative value indicates seeking backward through the file. Any combination of <i>nOffset</i> and <i>fuMode</i> that indicates seeking to a position before the beginning of the file or after the end of the file is not valid, and causes the method to return E_INVALIDARG.


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
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Seek is not implemented on this device.

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
 




## -remarks



The seek position is defined by passing either an <a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage</a> interface pointing to a location on a storage medium of the device, or an <a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation</a> interface that has been implemented to support streaming audio. The <b>IWMDMObjectInfo</b> interface can also be passed to describe some point within the object to which the specified interface points.

For device playback, if <b>Seek</b> is not called before <a href="https://msdn.microsoft.com/e8d717e6-365c-44ad-b24e-daa3c35664de">Play</a>, then playback starts at the first audio track on the first storage medium on the media device.

For device recording, if <b>Seek</b> is not called before <a href="https://msdn.microsoft.com/a9372ce9-e339-4664-9e12-4feae29529dc">Record</a>, the record operation fails. The recording length can be limited by calling the <a href="https://msdn.microsoft.com/7dfa6443-4eb8-4a88-8af1-c082750e8d22">IWMDMObjectInfo::SetPlayLength</a> method after returning from the <b>Seek</b> call.




## -see-also




<a href="https://msdn.microsoft.com/e7b58957-4795-461f-ae3d-fb80e6711c9f">IWMDMDeviceControl Interface</a>



<a href="https://msdn.microsoft.com/ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a">IWMDMObjectInfo Interface</a>



<a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation Interface</a>



<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>
 

 

