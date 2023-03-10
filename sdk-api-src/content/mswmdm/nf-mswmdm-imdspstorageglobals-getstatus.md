---
UID: NF:mswmdm.IMDSPStorageGlobals.GetStatus
title: IMDSPStorageGlobals::GetStatus (mswmdm.h)
description: The GetStatus method retrieves the current status of the storage medium.
helpviewer_keywords: ["GetStatus","GetStatus method [windows Media Device Manager]","GetStatus method [windows Media Device Manager]","IMDSPStorageGlobals interface","IMDSPStorageGlobals interface [windows Media Device Manager]","GetStatus method","IMDSPStorageGlobals.GetStatus","IMDSPStorageGlobals::GetStatus","IMDSPStorageGlobalsGetStatus","mswmdm/IMDSPStorageGlobals::GetStatus","wmdm.imdspstorageglobals_getstatus"]
old-location: wmdm\imdspstorageglobals_getstatus.htm
tech.root: WMDM
ms.assetid: 572b5de6-62d7-450f-851f-d09b1864a86c
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [windows Media Device Manager], GetStatus method [windows Media Device Manager],IMDSPStorageGlobals interface, IMDSPStorageGlobals interface [windows Media Device Manager],GetStatus method, IMDSPStorageGlobals.GetStatus, IMDSPStorageGlobals::GetStatus, IMDSPStorageGlobalsGetStatus, mswmdm/IMDSPStorageGlobals::GetStatus, wmdm.imdspstorageglobals_getstatus
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
 - IMDSPStorageGlobals::GetStatus
 - mswmdm/IMDSPStorageGlobals::GetStatus
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
 - IMDSPStorageGlobals.GetStatus
---

# IMDSPStorageGlobals::GetStatus


## -description

The <b>GetStatus</b> method retrieves the current status of the storage medium.

## -parameters

### -param pdwStatus [out]

Pointer to a <b>DWORD</b> containing the status information. The following status values can be returned by the <i>pdwStatus</i> parameter.

<table>
<tr>
<th>Status
                </th>
<th>Description
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
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

You must always call this method before attempting to interact with a storage medium. The status value returned is WMDM_STATUS_BUSY if some other interface has invoked an ongoing operation. You can evaluate the value returned from this call to determine whether an ongoing operation has been invoked from the <b>IMDSPStorageGlobals</b> interface.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals">IMDSPStorageGlobals Interface</a>