---
UID: NF:mprapi.MprAdminBufferFree
title: MprAdminBufferFree function
author: windows-sdk-content
description: The MprAdminBufferFree function frees memory buffers returned by:\_MprAdminDeviceEnum, MprAdminInterfaceGetInfo, MprAdminInterfaceDeviceGetInfo, MprAdminInterfaceEnum, MprAdminServerGetInfo, MprAdminInterfaceTransportGetInfo, and MprAdminTransportGetInfo.
old-location: rras\mpradminbufferfree.htm
tech.root: rras
ms.assetid: 60cae055-841a-4435-bf0e-4198b1ccdd4e
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: MprAdminBufferFree, MprAdminBufferFree function [RAS], _mpr_mpradminbufferfree, mprapi/MprAdminBufferFree, rras.mpradminbufferfree
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
 - MprAdminBufferFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminBufferFree function


## -description


The 
<b>MprAdminBufferFree</b> function frees memory buffers returned by: 
<a href="https://msdn.microsoft.com/092892fd-1b61-45c6-a05f-83fc193611b9">MprAdminDeviceEnum</a>, <a href="https://msdn.microsoft.com/a6d353f0-1d68-4a37-89f3-cdab0fc7972a">MprAdminInterfaceGetInfo</a>, 
<a href="https://msdn.microsoft.com/edff88dd-80ae-4704-b320-925006346dda">MprAdminInterfaceDeviceGetInfo</a>, <a href="https://msdn.microsoft.com/50486ad3-2f1d-4ab9-9a7f-7b72128486fb">MprAdminInterfaceEnum</a>, 
<a href="https://msdn.microsoft.com/d15dfb60-1239-4552-985f-d3c98f2981f4">MprAdminServerGetInfo</a>, 
<a href="https://msdn.microsoft.com/4e8d7fdf-668e-496a-977a-7a0306173495">MprAdminInterfaceTransportGetInfo</a>, and 
<a href="https://msdn.microsoft.com/47fbe483-8a1b-4747-9555-931dd63e2db8">MprAdminTransportGetInfo</a>.


## -parameters




### -param pBuffer [in]

Pointer to the memory buffer to free.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is the following error code.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pBuffer</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/50486ad3-2f1d-4ab9-9a7f-7b72128486fb">MprAdminInterfaceEnum</a>



<a href="https://msdn.microsoft.com/a6d353f0-1d68-4a37-89f3-cdab0fc7972a">MprAdminInterfaceGetInfo</a>



<a href="https://msdn.microsoft.com/4e8d7fdf-668e-496a-977a-7a0306173495">MprAdminInterfaceTransportGetInfo</a>



<a href="https://msdn.microsoft.com/d15dfb60-1239-4552-985f-d3c98f2981f4">MprAdminServerGetInfo</a>



<a href="https://msdn.microsoft.com/47fbe483-8a1b-4747-9555-931dd63e2db8">MprAdminTransportGetInfo</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

