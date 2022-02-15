---
UID: NE:exdisp.ShellWindowFindWindowOptions
title: ShellWindowFindWindowOptions (exdisp.h)
description: Specifies options for finding window in the Shell windows collection.
helpviewer_keywords: ["SWFO_COOKIEPASSED","SWFO_INCLUDEPENDING","SWFO_NEEDDISPATCH","ShellWindowFindWindowOptions","ShellWindowFindWindowOptions enumeration [Windows Shell]","_win32_ShellWindowFindWindowOptions","exdisp/SWFO_COOKIEPASSED","exdisp/SWFO_INCLUDEPENDING","exdisp/SWFO_NEEDDISPATCH","exdisp/ShellWindowFindWindowOptions","shell.ShellWindowFindWindowOptions"]
old-location: shell\ShellWindowFindWindowOptions.htm
tech.root: shell
ms.assetid: 2459ab16-56c0-4812-bc61-4a17978b04f3
ms.date: 12/05/2018
ms.keywords: SWFO_COOKIEPASSED, SWFO_INCLUDEPENDING, SWFO_NEEDDISPATCH, ShellWindowFindWindowOptions, ShellWindowFindWindowOptions enumeration [Windows Shell], _win32_ShellWindowFindWindowOptions, exdisp/SWFO_COOKIEPASSED, exdisp/SWFO_INCLUDEPENDING, exdisp/SWFO_NEEDDISPATCH, exdisp/ShellWindowFindWindowOptions, shell.ShellWindowFindWindowOptions
req.header: exdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ExDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ShellWindowFindWindowOptions
req.redist: 
req.product: Internet Explorer 5
ms.custom: 19H1
f1_keywords:
 - ShellWindowFindWindowOptions
 - exdisp/ShellWindowFindWindowOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ExDisp.h
api_name:
 - ShellWindowFindWindowOptions
---

# ShellWindowFindWindowOptions enumeration


## -description

Specifies options for finding window in the Shell windows collection.

## -enum-fields

### -field SWFO_NEEDDISPATCH:0x1

The window must have an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface.

### -field SWFO_INCLUDEPENDING:0x2

Include windows that were registered with <a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-registerpending">IShellWindows::RegisterPending</a>.

### -field SWFO_COOKIEPASSED:0x4

Causes <a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-findwindowsw">IShellWindows::FindWindowSW</a> to interpret <i>pvarLoc</i>  as a cookie rather than a PIDL.

## -see-also

<a href="/windows/desktop/api/exdisp/nn-exdisp-ishellwindows">IShellWindows</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-findwindowsw">IShellWindows::FindWindowSW</a>
