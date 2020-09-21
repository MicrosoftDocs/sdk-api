---
UID: NF:winwlx.WlxScreenSaverNotify
title: WlxScreenSaverNotify function (winwlx.h)
description: Winlogon calls this function immediately before a screen saver is activated, allowing the GINA to interact with the screen saver program.
helpviewer_keywords: ["WlxScreenSaverNotify","WlxScreenSaverNotify function [Security]","_gina_wlxscreensavernotify","security.wlxscreensavernotify","winwlx/WlxScreenSaverNotify"]
old-location: security\wlxscreensavernotify.htm
tech.root: security
ms.assetid: 72ed356d-bae3-42ac-87c2-99305951e24b
ms.date: 12/05/2018
ms.keywords: WlxScreenSaverNotify, WlxScreenSaverNotify function [Security], _gina_wlxscreensavernotify, security.wlxscreensavernotify, winwlx/WlxScreenSaverNotify
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
 - WlxScreenSaverNotify
 - winwlx/WlxScreenSaverNotify
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
 - WlxScreenSaverNotify
---

# WlxScreenSaverNotify function


## -description

<p class="CCE_Message">[The WlxScreenSaverNotify function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxScreenSaverNotify</b> function may be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function immediately before a screen saver is activated, allowing the GINA to interact with the screen saver program.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pWlxContext [in]

A pointer to the <a href="/windows/desktop/SecGloss/g-gly">GINA</a> context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> for this station.

### -param pSecure [in, out]

 A pointer to a Boolean value that, on input, specifies whether the current screen saver is secure and,  


on output, indicates whether the workstation should be locked.

## -returns

If the screen saver should be activated, the function returns <b>TRUE</b>.

If the screen saver should not be activated, the function returns <b>FALSE</b>.

## -remarks

If your GINA DLL does not export this function, Winlogon uses the following default behavior.


```cpp
#include <windows.h>
#include <Winwlx.h>

BOOL DefaultScreenSaverNotify(
   PVOID   pWlxContext,
   BOOL    *pSecure)
{
  if (*pSecure)
  {
    *pSecure = WlxIsLockOk(pWlxContext);
  }
  return(TRUE);
}

```


Before calling <b>WlxScreenSaverNotify</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>