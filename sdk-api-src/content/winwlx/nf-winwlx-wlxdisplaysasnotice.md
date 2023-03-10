---
UID: NF:winwlx.WlxDisplaySASNotice
title: WlxDisplaySASNotice function (winwlx.h)
description: Winlogon calls this function when no user is logged on.
helpviewer_keywords: ["WlxDisplaySASNotice","WlxDisplaySASNotice function [Security]","_gina_wlxdisplaysasnotice","security.wlxdisplaysasnotice","winwlx/WlxDisplaySASNotice"]
old-location: security\wlxdisplaysasnotice.htm
tech.root: security
ms.assetid: 2b56c037-aae6-4cb7-932f-15cf18c4444a
ms.date: 12/05/2018
ms.keywords: WlxDisplaySASNotice, WlxDisplaySASNotice function [Security], _gina_wlxdisplaysasnotice, security.wlxdisplaysasnotice, winwlx/WlxDisplaySASNotice
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
 - WlxDisplaySASNotice
 - winwlx/WlxDisplaySASNotice
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
 - WlxDisplaySASNotice
---

# WlxDisplaySASNotice function


## -description

<p class="CCE_Message">[The WlxDisplaySASNotice function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxDisplaySASNotice</b> function must be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function when no user is logged on.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. This is the context value that the GINA returns when Winlogon calls 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> for this station.

## -remarks

Before calling <b>WlxDisplaySASNotice</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>