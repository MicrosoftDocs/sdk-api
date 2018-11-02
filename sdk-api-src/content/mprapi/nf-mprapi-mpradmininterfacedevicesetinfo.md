---
UID: NF:mprapi.MprAdminInterfaceDeviceSetInfo
title: MprAdminInterfaceDeviceSetInfo function
author: windows-sdk-content
description: The MprAdminInterfaceDeviceSetInfo creates or modifies a device that is used in a router demand-dial interface.
old-location: rras\mpradmininterfacedevicesetinfo.htm
tech.root: rras
ms.assetid: ae8b3762-f176-4f91-97fc-33f7a9dcd424
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MprAdminInterfaceDeviceSetInfo, MprAdminInterfaceDeviceSetInfo function [RAS], _mpr_mpradmininterfacedevicesetinfo, mprapi/MprAdminInterfaceDeviceSetInfo, rras.mpradmininterfacedevicesetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminInterfaceDeviceSetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminInterfaceDeviceSetInfo function


## -description


The 
<b>MprAdminInterfaceDeviceSetInfo</b> creates or modifies a device that is used in a router demand-dial interface.


## -parameters




### -param hMprServer [in]

Handle to the  router on which to execute this call. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


### -param hInterface [in]

Handle to the interface. Obtain this handle from a previous call to 
<a href="https://msdn.microsoft.com/c9590ebe-7e49-4ad1-bd9b-0d9c51938bc4">MprAdminInterfaceCreate</a>, or by calling 
<a href="https://msdn.microsoft.com/50486ad3-2f1d-4ab9-9a7f-7b72128486fb">MprAdminInterfaceEnum</a>.


### -param dwIndex [in]

Specifies the one-based index of the device. A multi-linked demand-dial interface uses multiple devices.


### -param dwLevel [in]

A DWORD value that describes the format in which the information is structured in the <i>lplpBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0 or 1 as listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
</tr>
<tr>
<td>0</td>
<td>
<a href="https://msdn.microsoft.com/1814c428-1a3c-45f3-8b15-182e1eceff7b">MPR_DEVICE_0</a>
</td>
</tr>
<tr>
<td>1</td>
<td>
<a href="https://msdn.microsoft.com/99245e45-114d-4933-9189-cd45a1c22a96">MPR_DEVICE_1</a>
</td>
</tr>
</table>
 


### -param lpbBuffer [in]

A pointer to a <a href="https://msdn.microsoft.com/1814c428-1a3c-45f3-8b15-182e1eceff7b">MPR_DEVICE_0</a> or <a href="https://msdn.microsoft.com/99245e45-114d-4933-9189-cd45a1c22a96">MPR_DEVICE_1</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.
					


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling application does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hInterface</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lplpBuffer</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient resources to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwLevel</i> value is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1814c428-1a3c-45f3-8b15-182e1eceff7b">MPR_DEVICE_0</a>



<a href="https://msdn.microsoft.com/99245e45-114d-4933-9189-cd45a1c22a96">MPR_DEVICE_1</a>



<a href="https://msdn.microsoft.com/c9590ebe-7e49-4ad1-bd9b-0d9c51938bc4">MprAdminInterfaceCreate</a>



<a href="https://msdn.microsoft.com/edff88dd-80ae-4704-b320-925006346dda">MprAdminInterfaceDeviceGetInfo</a>
 

 

