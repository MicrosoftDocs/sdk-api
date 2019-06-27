---
UID: NF:mprapi.MprAdminMIBBufferFree
title: MprAdminMIBBufferFree function (mprapi.h)
author: windows-sdk-content
description: The MprAdminMIBBufferFree function frees buffers returned by the following functions MprAdminMIBEntryGet, MprAdminMIBEntryGetFirst, MprAdminMIBEntryGetNext
old-location: rras\mpradminmibbufferfree.htm
tech.root: RRAS
ms.assetid: cee21427-42bc-45df-ad95-c8aa81041776
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MprAdminMIBBufferFree, MprAdminMIBBufferFree function [RAS], _mpr_mpradminmibbufferfree, mprapi/MprAdminMIBBufferFree, rras.mpradminmibbufferfree
ms.topic: function
f1_keywords: 
 - "mprapi/MprAdminMIBBufferFree"
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
 - MprAdminMIBBufferFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprAdminMIBBufferFree function


## -description


The 
<b>MprAdminMIBBufferFree</b> function frees buffers returned by the following functions:
<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminmibentryget">MprAdminMIBEntryGet</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminmibentrygetfirst">MprAdminMIBEntryGetFirst</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminmibentrygetnext">MprAdminMIBEntryGetNext</a>
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




<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminmibentryget">MprAdminMIBEntryGet</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminmibentrygetfirst">MprAdminMIBEntryGetFirst</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminmibentrygetnext">MprAdminMIBEntryGetNext</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/mib-functions">Router Management MIB Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-management-mib-reference">Router Management MIB Reference</a>
 

 

