---
UID: NF:winwlx.WlxInitialize
title: WlxInitialize function (winwlx.h)
description: Winlogon calls this function once for each window station present on the computer. Currently, the operating system supports one window station per workstation.
helpviewer_keywords: ["WLX_DISPATCH_VERSION_1_0","WLX_DISPATCH_VERSION_1_1","WLX_DISPATCH_VERSION_1_2","WLX_DISPATCH_VERSION_1_3","WLX_DISPATCH_VERSION_1_4","WlxInitialize","WlxInitialize function [Security]","_gina_wlxinitialize","security.wlxinitialize","winwlx/WlxInitialize"]
old-location: security\wlxinitialize.htm
tech.root: security
ms.assetid: db03f2b3-0719-40be-8a42-04ab7110f711
ms.date: 12/05/2018
ms.keywords: WLX_DISPATCH_VERSION_1_0, WLX_DISPATCH_VERSION_1_1, WLX_DISPATCH_VERSION_1_2, WLX_DISPATCH_VERSION_1_3, WLX_DISPATCH_VERSION_1_4, WlxInitialize, WlxInitialize function [Security], _gina_wlxinitialize, security.wlxinitialize, winwlx/WlxInitialize
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
 - WlxInitialize
 - winwlx/WlxInitialize
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
 - WlxInitialize
---

# WlxInitialize function


## -description

<p class="CCE_Message">[The WlxInitialize function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxInitialize</b> function must be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function once for each window station present on the computer. Currently, the operating system supports one window station per workstation.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>The <a href="/windows/desktop/SecGloss/c-gly">context</a> returned by this function will be passed back to the GINA in all subsequent calls.

## -parameters

### -param lpWinsta [in]

A pointer to the name of the window station being initialized.

### -param hWlx [in]

A handle to Winlogon. The GINA must supply this handle in all calls to Winlogon support functions that involve this window station.

### -param pvReserved [in]

This parameter is reserved for future use and must be set to <b>NULL</b>.

### -param pWinlogonFunctions [in]

A pointer to a Winlogon support function dispatch table. The contents of the table depend on the GINA DLL version returned by the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a> call. This table does not change, which allows the GINA DLL to reference the table without copying it. If the GINA DLL needs to make a copy of the table, it should call <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_get_option">WlxGetOption</a> and supply WLX_OPTION_DISPATCH_TABLE_SIZE for the <b>Option</b> parameter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLX_DISPATCH_VERSION_1_4"></a><a id="wlx_dispatch_version_1_4"></a><dl>
<dt><b><a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_4">WLX_DISPATCH_VERSION_1_4</a></b></dt>
</dl>
</td>
<td width="60%">
Winlogon dispatch table - version 1.4

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_DISPATCH_VERSION_1_3"></a><a id="wlx_dispatch_version_1_3"></a><dl>
<dt><b><a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_3">WLX_DISPATCH_VERSION_1_3</a></b></dt>
</dl>
</td>
<td width="60%">
Winlogon dispatch table - version 1.3

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_DISPATCH_VERSION_1_2"></a><a id="wlx_dispatch_version_1_2"></a><dl>
<dt><b><a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_2">WLX_DISPATCH_VERSION_1_2</a></b></dt>
</dl>
</td>
<td width="60%">
Winlogon dispatch table - version 1.2

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_DISPATCH_VERSION_1_1"></a><a id="wlx_dispatch_version_1_1"></a><dl>
<dt><b><a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_1">WLX_DISPATCH_VERSION_1_1</a></b></dt>
</dl>
</td>
<td width="60%">
Winlogondispatch table - version 1.1

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_DISPATCH_VERSION_1_0"></a><a id="wlx_dispatch_version_1_0"></a><dl>
<dt><b><a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_0">WLX_DISPATCH_VERSION_1_0</a></b></dt>
</dl>
</td>
<td width="60%">
Winlogon dispatch table - version 1.0

</td>
</tr>
</table>

### -param pWlxContext [out]

A pointer to a pointer to a <b>VOID</b> that will contain the address of the GINA context for this window station. This context is passed in all subsequent calls to the GINA from Winlogon. The GINA DLL manages any memory used by the context. The context pointer can be changed later by calling the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_set_option">WlxSetOption</a> function with WLX_OPTION_CONTEXT_POINTER.

## -returns

If the function successfully initializes the GINA DLL, the function returns <b>TRUE</b>.

If the function fails, or if the GINA DLL was not initialized, the function returns <b>FALSE</b>. Winlogon will terminate, and the system will not boot.

## -remarks

<b>WlxInitialize</b> is called once for each window station present on the computer.

Currently only a single window station called Winsta0 is supported.

Before calling <b>WlxInitialize</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a>