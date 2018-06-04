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

# IMDSPStorageGlobals::GetStatus


## -description



The <b>GetStatus</b> method retrieves the current status of the storage medium.




## -parameters




### -param pdwStatus [out]

Pointer to a <b>DWORD</b> containing the status information. The following status values can be returned by the <i>pdwStatus</i> parameter.

<table>
<tr>
<th>
                  Status
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>WMDM_STATUS_READY</td>
<td>The medium is in an idle ready state.</td>
</tr>
<tr>
<td>WMDM_STATUS_BUSY</td>
<td>An operation is ongoing. Evaluate status values to determine the ongoing operation.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_NOTPRESENT</td>
<td>The medium is not present. For devices that support more than one medium, this value is only reported from the <b>IMDSPStorageGlobals</b> interface.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_INITIALIZING</td>
<td>The device is currently busy formatting media on a device.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_BROKEN</td>
<td>The medium is broken. For devices that support more than one medium, this value is only reported from the <b>IMDSPStorageGlobals</b> interface.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_NOTSUPPORTED</td>
<td>The medium is not supported by the device. For devices that support more than one medium, this value is only returned from the <b>IMDSPStorageGlobals</b> interface.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_UNFORMATTED</td>
<td>The medium is not formatted. For devices that support more than one medium, this value is only reported from the <b>IMDSPStorageGlobals</b> interface.</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



You must always call this method before attempting to interact with a storage medium. The status value returned is WMDM_STATUS_BUSY if some other interface has invoked an ongoing operation. You can evaluate the value returned from this call to determine whether an ongoing operation has been invoked from the <b>IMDSPStorageGlobals</b> interface.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/70653352-a467-4197-93e3-e8fb45f99d34">IMDSPStorageGlobals Interface</a>
 

 

