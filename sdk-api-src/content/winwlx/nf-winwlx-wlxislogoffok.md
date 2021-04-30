---
UID: NF:winwlx.WlxIsLogoffOk
title: WlxIsLogoffOk function (winwlx.h)
description: Winlogon calls this function when the user initiates a logoff operation.
helpviewer_keywords: ["WlxIsLogoffOk","WlxIsLogoffOk function [Security]","_gina_wlxislogoffok","security.wlxislogoffok","winwlx/WlxIsLogoffOk"]
old-location: security\wlxislogoffok.htm
tech.root: security
ms.assetid: fe718ae7-d19e-430c-8d84-41682dca30a1
ms.date: 12/05/2018
ms.keywords: WlxIsLogoffOk, WlxIsLogoffOk function [Security], _gina_wlxislogoffok, security.wlxislogoffok, winwlx/WlxIsLogoffOk
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WlxIsLogoffOk
 - winwlx/WlxIsLogoffOk
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winwlx.h
api_name:
 - WlxIsLogoffOk
---

# WlxIsLogoffOk function


## -description

<p class="CCE_Message">[The WlxIsLogoffOk function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxIsLogoffOk</b> function must be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function when the user initiates a logoff operation.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pWlxContext [in]

Pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> for this station.

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
Returns <b>TRUE</b> if it is acceptable to perform the logoff operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Returns <b>FALSE</b> if it is not acceptable to perform the logoff operation.

</td>
</tr>
</table>

## -remarks

<b>WlxIsLogoffOk</b> can return <b>FALSE</b> to prevent the user from logging off the workstation.

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>