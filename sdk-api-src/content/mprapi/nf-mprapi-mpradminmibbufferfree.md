---
UID: NF:mprapi.MprAdminMIBBufferFree
title: MprAdminMIBBufferFree function
author: windows-sdk-content
description: The MprAdminMIBBufferFree function frees buffers returned by the following functions:
old-location: rras\mpradminmibbufferfree.htm
old-project: rras
ms.assetid: cee21427-42bc-45df-ad95-c8aa81041776
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: MprAdminMIBBufferFree, MprAdminMIBBufferFree function [RAS], _mpr_mpradminmibbufferfree, mprapi/MprAdminMIBBufferFree, rras.mpradminmibbufferfree
ms.prod: windows
ms.technology: windows-sdk
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
 - MprAdminMIBBufferFree
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminMIBBufferFree function


## -description


The 
<b>MprAdminMIBBufferFree</b> function frees buffers returned by the following functions:
<ul>
<li>
<a href="https://msdn.microsoft.com/98e88364-4757-4b43-8316-6d4d9b3c2f29">MprAdminMIBEntryGet</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e3c3ac47-d47c-4fd4-a064-b737bc40f190">MprAdminMIBEntryGetFirst</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e73dcb-db73-4415-8275-88f9ae010ab7">MprAdminMIBEntryGetNext</a>
</li>
</ul>

## -parameters




### -param pBuffer [in]

Pointer to a memory buffer to free.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
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
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/98e88364-4757-4b43-8316-6d4d9b3c2f29">MprAdminMIBEntryGet</a>



<a href="https://msdn.microsoft.com/e3c3ac47-d47c-4fd4-a064-b737bc40f190">MprAdminMIBEntryGetFirst</a>



<a href="https://msdn.microsoft.com/31e73dcb-db73-4415-8275-88f9ae010ab7">MprAdminMIBEntryGetNext</a>



<a href="https://msdn.microsoft.com/c911daa4-4f3d-4944-9dc0-695a4efbcb1b">Router Management MIB Functions</a>



<a href="https://msdn.microsoft.com/a7a28ac0-c6f9-450c-9925-67990a62ba08">Router Management MIB Reference</a>
 

 

