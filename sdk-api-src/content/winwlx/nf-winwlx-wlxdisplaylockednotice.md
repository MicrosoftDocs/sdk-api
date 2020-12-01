---
UID: NF:winwlx.WlxDisplayLockedNotice
title: WlxDisplayLockedNotice function (winwlx.h)
description: Allows the GINA to display information about the lock, such as who locked the workstation and when it was locked.
helpviewer_keywords: ["WlxDisplayLockedNotice","WlxDisplayLockedNotice function [Security]","_gina_wlxdisplaylockednotice","security.wlxdisplaylockednotice","winwlx/WlxDisplayLockedNotice"]
old-location: security\wlxdisplaylockednotice.htm
tech.root: security
ms.assetid: f8209ac4-e79b-4997-8dc3-c9224e10822b
ms.date: 12/05/2018
ms.keywords: WlxDisplayLockedNotice, WlxDisplayLockedNotice function [Security], _gina_wlxdisplaylockednotice, security.wlxdisplaylockednotice, winwlx/WlxDisplayLockedNotice
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
 - WlxDisplayLockedNotice
 - winwlx/WlxDisplayLockedNotice
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
 - WlxDisplayLockedNotice
---

# WlxDisplayLockedNotice function


## -description

<p class="CCE_Message">[The WlxDisplayLockedNotice function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Allows the GINA to display information about the lock, such as who locked the workstation and when it was locked.

The <b>WlxDisplayLockedNotice</b> function must be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function when the workstation is placed in the locked state.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pWlxContext [in]

Pointer to the GINA context associated with this window station. This is the context value that the GINA returns when Winlogon calls 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> for this station.

## -remarks

To display lock information, the GINA must display a dialog box that will be interrupted by a WLX_WM_SAS message. For more information, see 
<a href="/windows/desktop/SecAuthN/sending-messages-to-the-gina">Sending Messages to the GINA</a>.

Before calling <b>WlxDisplayLockedNotice</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxdisplaysasnotice">WlxDisplaySASNotice</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>