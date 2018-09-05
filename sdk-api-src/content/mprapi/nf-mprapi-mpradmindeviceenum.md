---
UID: NF:mprapi.MprAdminDeviceEnum
title: MprAdminDeviceEnum function
author: windows-sdk-content
description: Function is called to enumerate RAS capable devices installed on the computer that can return their name and type.
old-location: rras\mpradmindeviceenum.htm
old-project: RRAS
ms.assetid: 092892fd-1b61-45c6-a05f-83fc193611b9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: MprAdminDeviceEnum, MprAdminDeviceEnum function [RAS], mprapi/MprAdminDeviceEnum, rras.mpradmindeviceenum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminDeviceEnum
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminDeviceEnum function


## -description


The <b>MprAdminDeviceEnum</b>function is called to enumerate RAS capable devices installed on the computer that can return their name and type.


## -parameters




### -param hMprServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


### -param dwLevel [in]

A DWORD value that describes the format in which the information is returned in the <i>lplpbBuffer</i> parameter. Must be zero.


### -param lplpbBuffer [out]

On successful completion, an array of <a href="https://msdn.microsoft.com/1814c428-1a3c-45f3-8b15-182e1eceff7b">MPR_DEVICE_0</a> structures that contains the RAS capable device information. Free this memory by calling 
<a href="https://msdn.microsoft.com/60cae055-841a-4435-bf0e-4198b1ccdd4e">MprAdminBufferFree</a>.


### -param lpdwTotalEntries [out]

The number of entries of type <a href="https://msdn.microsoft.com/1814c428-1a3c-45f3-8b15-182e1eceff7b">MPR_DEVICE_0</a> in <i>lplpbBuffer</i>. 


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
<dt><b>ERROR_NOT_SUPPORTED </b></dt>
</dl>
</td>
<td width="60%">
The <i>dwlevel</i> parameter does not equal zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER </b></dt>
</dl>
</td>
<td width="60%">
The <i>lplpbBuffer</i> or <i>lpdwTotalEntries</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

