---
UID: NF:mswmdm.IMDSPDevice.GetType
title: IMDSPDevice::GetType
author: windows-sdk-content
description: The GetType method retrieves device type information.
old-location: wmdm\imdspdevice_gettype.htm
tech.root: WMDM
ms.assetid: 15e598bb-bcc9-4254-aa1c-24d7dd6b97a8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetType, GetType method [windows Media Device Manager], GetType method [windows Media Device Manager],IMDSPDevice interface, IMDSPDevice interface [windows Media Device Manager],GetType method, IMDSPDevice.GetType, IMDSPDevice::GetType, IMDSPDeviceGetType, mswmdm/IMDSPDevice::GetType, wmdm.imdspdevice_gettype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPDevice.GetType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPDevice::GetType


## -description



The <b>GetType</b> method retrieves device type information.




## -parameters




### -param pdwType [out]

Pointer to a <b>DWORD</b> that receives the type attributes of the device. The following table shows the types received.

<table>
<tr>
<th>Device type
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_PLAYBACK</td>
<td>The media device supports audio playback.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_RECORD</td>
<td>The media device supports audio recording.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_DECODE</td>
<td>The media device supports audio format decoding.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_ENCODE</td>
<td>The media device supports audio format encoding.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_STORAGE</td>
<td>The media device has on-board storage for media files.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_SDMI</td>
<td>The media device is SDMI compliant.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_NONSDMI</td>
<td>The media device is not SDMI compliant.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_VIRTUAL</td>
<td>The media device is not a physical device.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_NONREENTRANT</td>
<td>The media device must synchronize access to the service provider services.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_FILELISTRESYNC</td>
<td>The media device allows the file list to be resynchronized.</td>
</tr>
<tr>
<td>WMDM_DEVICE_TYPE_VIEW_PREF_METADATAVIEW</td>
<td>The media device prefers metadata views while its storages are enumerated.</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice Interface</a>



<a href="https://msdn.microsoft.com/bc4fef6e-8faf-4114-a68d-bbc30bc18130">IMDSPDevice::GetName</a>
 

 

