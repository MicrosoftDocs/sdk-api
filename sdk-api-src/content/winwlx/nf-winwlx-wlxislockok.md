---
UID: NF:winwlx.WlxIsLockOk
title: WlxIsLockOk function
author: windows-sdk-content
description: Winlogon calls this function before attempting to lock the workstation.
old-location: security\wlxislockok.htm
tech.root: SecAuthN
ms.assetid: 764d7fc9-57d8-472a-9b91-ebfbe3628452
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: WlxIsLockOk, WlxIsLockOk function [Security], _gina_wlxislockok, security.wlxislockok, winwlx/WlxIsLockOk
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winwlx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winwlx.h
api_name:
 - WlxIsLockOk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WlxIsLockOk
: 
---

# WlxIsLockOk function


## -description


<p class="CCE_Message">[The WlxIsLockOk function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxIsLockOk</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> calls this function before attempting to lock the workstation.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

Pointer to the GINA context associated with this window station. The GINA supplies this context when Winlogon calls 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Returns <b>TRUE</b> if it is acceptable to lock the workstation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Returns <b>FALSE</b> if it is not acceptable to lock the workstation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

