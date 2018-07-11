---
UID: NF:mswmdm.IWMDMStorageGlobals.GetStatus
title: IWMDMStorageGlobals::GetStatus
author: windows-sdk-content
description: The GetStatus method retrieves the current status of a storage medium.
old-location: wmdm\iwmdmstorageglobals_getstatus.htm
old-project: WMDM
ms.assetid: cfb6d233-6fc0-4589-9324-f4242798afc5
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetStatus, GetStatus method [windows Media Device Manager], GetStatus method [windows Media Device Manager],IWMDMStorageGlobals interface, IWMDMStorageGlobals interface [windows Media Device Manager],GetStatus method, IWMDMStorageGlobals.GetStatus, IWMDMStorageGlobals::GetStatus, IWMDMStorageGlobalsGetStatus, mswmdm/IWMDMStorageGlobals::GetStatus, wmdm.iwmdmstorageglobals_getstatus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMStorageGlobals.GetStatus
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorageGlobals::GetStatus


## -description



The <b>GetStatus</b> method retrieves the current status of a storage medium.




## -parameters




### -param pdwStatus [out]

Pointer to a <b>DWORD</b> to receive the status information when the method returns. The following values can be returned in the <i>pdwStatus</i> parameter.

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
<td>The medium is in an idle or ready state.</td>
</tr>
<tr>
<td>WMDM_STATUS_BUSY</td>
<td>An operation is ongoing. Evaluate status values to determine the ongoing operation.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_NOTPRESENT</td>
<td>The storage medium is not present. For devices with more than one medium supported, this value is only reported from the <b>IWMDMStorageGlobals</b> interface.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_INITIALIZING</td>
<td>The device is currently busy formatting a storage medium on a device.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_BROKEN</td>
<td>The storage medium is broken. For devices with more than one medium supported, this value is only reported from the <b>IWMDMStorageGlobals</b> interface.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_NOTSUPPORTED</td>
<td>The storage medium is not supported by the device. For devices with more than one medium supported, this value is only returned from the <b>IWMDMStorageGlobals</b> interface.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_UNFORMATTED</td>
<td>The storage medium is not formatted. For devices with more than one medium supported, this value is only reported from the <b>IWMDMStorageGlobals</b> interface.</td>
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



This method must always be called before the caller attempts to interact with a storage medium. The status value retrieved is WMDM_STATUS_BUSY if some other interface has invoked an ongoing operation. You can evaluate the value retrieved from this call to determine whether an ongoing operation has been invoked from the <b>IWMDMStorageGlobals</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/fe164271-58f0-4b28-a200-6b15f8b42d36">IWMDMStorageGlobals Interface</a>
 

 

