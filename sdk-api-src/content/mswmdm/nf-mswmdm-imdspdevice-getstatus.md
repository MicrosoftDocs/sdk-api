---
UID: NF:mswmdm.IMDSPDevice.GetStatus
title: IMDSPDevice::GetStatus
author: windows-sdk-content
description: The GetStatus method retrieves all the device status information that the device can provide.
old-location: wmdm\imdspdevice_getstatus.htm
old-project: WMDM
ms.assetid: 76c5ee43-4d21-436e-b193-8a8e034651f0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetStatus, GetStatus method [windows Media Device Manager], GetStatus method [windows Media Device Manager],IMDSPDevice interface, IMDSPDevice interface [windows Media Device Manager],GetStatus method, IMDSPDevice.GetStatus, IMDSPDevice::GetStatus, IMDSPDeviceGetStatus, mswmdm/IMDSPDevice::GetStatus, wmdm.imdspdevice_getstatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.redist: 
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
 - IMDSPDevice.GetStatus
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPDevice::GetStatus


## -description



The <b>GetStatus</b> method retrieves all the device status information that the device can provide.




## -parameters




### -param pdwStatus [out]

Pointer to a <b>DWORD</b> that receives the current device status. These status values are defined in the following table.

<table>
<tr>
<th>Status
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_STATUS_READY</td>
<td>Windows Media Device Manager and its subcomponents are in a ready state.</td>
</tr>
<tr>
<td>WMDM_STATUS_BUSY</td>
<td>An operation is ongoing. Check other status values to determine which operation it is.</td>
</tr>
<tr>
<td>WMDM_STATUS_DEVICE_NOTPRESENT</td>
<td>The device is not connected to the computer.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_NOTPRESENT</td>
<td>The medium is not present. For devices that support more than one medium, this value is reported only from the <a href="https://msdn.microsoft.com/fe164271-58f0-4b28-a200-6b15f8b42d36">IWMDMStorageGlobals</a> interface.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_INITIALIZING</td>
<td>The device is currently busy formatting media on the device.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_BROKEN</td>
<td>The medium is not working. For devices that support more than one medium, this value is reported only from the <b>IWMDMStorageGlobals</b> interface.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_NOTSUPPORTED</td>
<td>The medium is not supported by the device. For devices that support more than one medium, this value is returned only from the <b>IWMDMStorageGlobals</b> interface.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGE_UNFORMATTED</td>
<td>The medium is not formatted. For devices that support more than one medium, this value is returned only from the <b>IWMDMStorageGlobals</b> interface.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGECONTROL_INSERTING</td>
<td>The <a href="https://msdn.microsoft.com/909b94fd-99de-4e26-87d6-d074a6eb5da3">IWMDMStorageControl::Insert</a> method is currently running.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGECONTROL_DELETING</td>
<td>The <a href="https://msdn.microsoft.com/f2b044d2-6386-4c2e-a437-5ebddf827fb4">IWMDMStorageControl::Delete</a> method is currently running.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGECONTROL_MOVING</td>
<td>The <a href="https://msdn.microsoft.com/6a2cfca0-66e6-4358-99c1-161f7baccdd5">IWMDMStorageControl::Move</a> method is currently running.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGECONTROL_READING</td>
<td>The <a href="https://msdn.microsoft.com/4b102666-b54b-4b60-b2e9-68def384268e">IWMDMStorageControl::Read</a> method is currently running.</td>
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



One or more status values can be returned from this call. All the status values of all the interfaces of the media device are reported through this call. For example, if a storage operation, such as writing a file to a media device is ongoing, a call to this method reports the busy status of that operation. For any ongoing operation, the status value WMDM_STATUS_BUSY is always present.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice Interface</a>



<a href="https://msdn.microsoft.com/b56edc7a-0764-449a-95b4-da759e99fadd">IWMDMStorageControl Interface</a>



<a href="https://msdn.microsoft.com/fe164271-58f0-4b28-a200-6b15f8b42d36">IWMDMStorageGlobals Interface</a>
 

 

