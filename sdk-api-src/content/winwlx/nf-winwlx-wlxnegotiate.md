---
UID: NF:winwlx.WlxNegotiate
title: WlxNegotiate function (winwlx.h)
description: The WlxNegotiate function must be implemented by a replacement GINA DLL. This is the first call made by Winlogon to the GINA DLL. WlxNegotiate allows the GINA to verify that it supports the installed version of Winlogon.
helpviewer_keywords: ["WlxNegotiate","WlxNegotiate function [Security]","_gina_wlxnegotiate","security.wlxnegotiate","winwlx/WlxNegotiate"]
old-location: security\wlxnegotiate.htm
tech.root: security
ms.assetid: 9e7bab30-5cc6-4c55-82e4-d888e1af59ed
ms.date: 12/05/2018
ms.keywords: WlxNegotiate, WlxNegotiate function [Security], _gina_wlxnegotiate, security.wlxnegotiate, winwlx/WlxNegotiate
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
 - WlxNegotiate
 - winwlx/WlxNegotiate
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
 - WlxNegotiate
---

# WlxNegotiate function


## -description

<p class="CCE_Message">[The WlxNegotiate function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxNegotiate</b> function must be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. This is the first call made by <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> to the GINA DLL. <b>WlxNegotiate</b> allows the GINA to verify that it supports the installed version of Winlogon.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param dwWinlogonVersion [in]

Specifies which version of Winlogon will be communicating with the GINA.

### -param pdwDllVersion [out]

Indicates which version of Winlogon the GINA supports. This version information is also used by Winlogon to determine which dispatch table is passed to the GINA in subsequent calls to 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>. This version cannot be greater than the version specified by <i>dwWinLogonVersion</i>.

## -returns

If the Winlogon version specified by <i>dwWinLogonVersion</i> is greater than or equal to the version returned in <i>pdwDllVersion</i>, the function returns <b>TRUE</b>. When <b>TRUE</b> is returned, Winlogon will continue to initialize.

If <i>dwWinLogonVersion</i> is less than <i>pdwDllVersion</i>, the function returns <b>FALSE</b>. When <b>FALSE</b> is returned, Winlogon will terminate and the system will not boot.

## -remarks

Before calling <b>WlxNegotiate</b>, <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>