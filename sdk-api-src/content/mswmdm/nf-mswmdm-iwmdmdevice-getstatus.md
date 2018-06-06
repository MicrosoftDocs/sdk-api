---
UID: NF:mswmdm.IWMDMDevice.GetStatus
title: IWMDMDevice::GetStatus
author: windows-sdk-content
description: The GetStatus method retrieves device status information.
old-location: wmdm\iwmdmdevice_getstatus.htm
old-project: WMDM
ms.assetid: 18445ba5-6c91-4b4c-8f9b-b9d94fd96155
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetStatus, GetStatus method [windows Media Device Manager], GetStatus method [windows Media Device Manager],IWMDMDevice interface, IWMDMDevice interface [windows Media Device Manager],GetStatus method, IWMDMDevice.GetStatus, IWMDMDevice::GetStatus, IWMDMDeviceGetStatus, mswmdm/IWMDMDevice::GetStatus, wmdm.iwmdmdevice_getstatus
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
 - IWMDMDevice.GetStatus
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMDevice::GetStatus


## -description



The <b>GetStatus</b> method retrieves device status information.




## -parameters




### -param pdwStatus [out]

Pointer to a <b>DWORD</b> specifying the device status. The possible values returned in <i>pdwStatus</i> are provided in the following table.

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
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice Interface</a>
 

 

