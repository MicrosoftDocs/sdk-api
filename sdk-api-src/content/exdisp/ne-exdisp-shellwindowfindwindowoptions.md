---
UID: NE:exdisp.ShellWindowFindWindowOptions
title: ShellWindowFindWindowOptions (exdisp.h)
description: Specifies options for finding window in the Shell windows collection.
old-location: shell\ShellWindowFindWindowOptions.htm
tech.root: shell
ms.assetid: 2459ab16-56c0-4812-bc61-4a17978b04f3
ms.date: 12/05/2018
ms.keywords: SWFO_COOKIEPASSED, SWFO_INCLUDEPENDING, SWFO_NEEDDISPATCH, ShellWindowFindWindowOptions, ShellWindowFindWindowOptions enumeration [Windows Shell], _win32_ShellWindowFindWindowOptions, exdisp/SWFO_COOKIEPASSED, exdisp/SWFO_INCLUDEPENDING, exdisp/SWFO_NEEDDISPATCH, exdisp/ShellWindowFindWindowOptions, shell.ShellWindowFindWindowOptions
f1_keywords:
- exdisp/ShellWindowFindWindowOptions
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ExDisp.h
api_name:
- ShellWindowFindWindowOptions
targetos: Windows
req.typenames: ShellWindowFindWindowOptions
req.redist: 
req.product: Internet Explorer 5
ms.custom: 19H1
---

# ShellWindowFindWindowOptions enumeration


## -description


Specifies options for finding window in the Shell windows collection.
        


## -enum-fields




### -field SWFO_NEEDDISPATCH

The window must have an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. 
            


### -field SWFO_INCLUDEPENDING

Include windows that were registered with <a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-registerpending">IShellWindows::RegisterPending</a>.
            


### -field SWFO_COOKIEPASSED

Causes <a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-findwindowsw">IShellWindows::FindWindowSW</a> to interpret <i>pvarLoc</i>  as a cookie rather than a PIDL.
            


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nn-exdisp-ishellwindows">IShellWindows</a>



<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-findwindowsw">IShellWindows::FindWindowSW</a>
 

 

