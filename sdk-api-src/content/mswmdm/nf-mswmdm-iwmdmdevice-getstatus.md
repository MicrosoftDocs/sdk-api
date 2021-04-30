---
UID: NF:mswmdm.IWMDMDevice.GetStatus
title: IWMDMDevice::GetStatus (mswmdm.h)
description: The GetStatus method retrieves device status information.
helpviewer_keywords: ["GetStatus","GetStatus method [windows Media Device Manager]","GetStatus method [windows Media Device Manager]","IWMDMDevice interface","IWMDMDevice interface [windows Media Device Manager]","GetStatus method","IWMDMDevice.GetStatus","IWMDMDevice::GetStatus","IWMDMDeviceGetStatus","mswmdm/IWMDMDevice::GetStatus","wmdm.iwmdmdevice_getstatus"]
old-location: wmdm\iwmdmdevice_getstatus.htm
tech.root: WMDM
ms.assetid: 18445ba5-6c91-4b4c-8f9b-b9d94fd96155
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [windows Media Device Manager], GetStatus method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],GetStatus method, IWMDMDevice.GetStatus, IWMDMDevice::GetStatus, IWMDMDeviceGetStatus, mswmdm/IWMDMDevice::GetStatus, wmdm.iwmdmdevice_getstatus
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
 - IWMDMDevice::GetStatus
 - mswmdm/IWMDMDevice::GetStatus
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
 - IWMDMDevice.GetStatus
---

# IWMDMDevice::GetStatus


## -description

The <b>GetStatus</b> method retrieves device status information.

## -parameters

### -param pdwStatus [out]

Pointer to a <b>DWORD</b> specifying the device status. The possible values returned in <i>pdwStatus</i> are provided in the following table.

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
<td>An operation is ongoing. Evaluate status values to determine the operation.</td>
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

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice Interface</a>