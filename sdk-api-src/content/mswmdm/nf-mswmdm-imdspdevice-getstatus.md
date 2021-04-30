---
UID: NF:mswmdm.IMDSPDevice.GetStatus
title: IMDSPDevice::GetStatus (mswmdm.h)
description: The GetStatus method retrieves all the device status information that the device can provide.
helpviewer_keywords: ["GetStatus","GetStatus method [windows Media Device Manager]","GetStatus method [windows Media Device Manager]","IMDSPDevice interface","IMDSPDevice interface [windows Media Device Manager]","GetStatus method","IMDSPDevice.GetStatus","IMDSPDevice::GetStatus","IMDSPDeviceGetStatus","mswmdm/IMDSPDevice::GetStatus","wmdm.imdspdevice_getstatus"]
old-location: wmdm\imdspdevice_getstatus.htm
tech.root: WMDM
ms.assetid: 76c5ee43-4d21-436e-b193-8a8e034651f0
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [windows Media Device Manager], GetStatus method [windows Media Device Manager],IMDSPDevice interface, IMDSPDevice interface [windows Media Device Manager],GetStatus method, IMDSPDevice.GetStatus, IMDSPDevice::GetStatus, IMDSPDeviceGetStatus, mswmdm/IMDSPDevice::GetStatus, wmdm.imdspdevice_getstatus
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMDSPDevice::GetStatus
 - mswmdm/IMDSPDevice::GetStatus
dev_langs:
 - c++
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
<td>The medium is not present. For devices that support more than one medium, this value is reported only from the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals</a> interface.</td>
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
<td>The <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert">IWMDMStorageControl::Insert</a> method is currently running.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGECONTROL_DELETING</td>
<td>The <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete">IWMDMStorageControl::Delete</a> method is currently running.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGECONTROL_MOVING</td>
<td>The <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move">IWMDMStorageControl::Move</a> method is currently running.</td>
</tr>
<tr>
<td>WMDM_STATUS_STORAGECONTROL_READING</td>
<td>The <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read">IWMDMStorageControl::Read</a> method is currently running.</td>
</tr>
</table>

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

One or more status values can be returned from this call. All the status values of all the interfaces of the media device are reported through this call. For example, if a storage operation, such as writing a file to a media device is ongoing, a call to this method reports the busy status of that operation. For any ongoing operation, the status value WMDM_STATUS_BUSY is always present.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals Interface</a>