---
UID: NF:winwlx.WlxDisplayLockedNotice
title: WlxDisplayLockedNotice function
author: windows-driver-content
description: Allows the GINA to display information about the lock, such as who locked the workstation and when it was locked.
old-location: security\wlxdisplaylockednotice.htm
old-project: SecAuthN
ms.assetid: f8209ac4-e79b-4997-8dc3-c9224e10822b
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: WlxDisplayLockedNotice, WlxDisplayLockedNotice function [Security], _gina_wlxdisplaylockednotice, security.wlxdisplaylockednotice, winwlx/WlxDisplayLockedNotice
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
req.typenames: ICONINFOEXW, *PICONINFOEXW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winwlx.h
api_name:
-	WlxDisplayLockedNotice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlxDisplayLockedNotice function


## -description


<p class="CCE_Message">[The WlxDisplayLockedNotice function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Allows the GINA to display information about the lock, such as who locked the workstation and when it was locked.

The <b>WlxDisplayLockedNotice</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a> calls this function when the workstation is placed in the locked state.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

Pointer to the GINA context associated with this window station. This is the context value that the GINA returns when Winlogon calls 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> for this station.


## -returns



This function has no return values.




## -remarks



To display lock information, the GINA must display a dialog box that will be interrupted by a WLX_WM_SAS message. For more information, see 
<a href="https://msdn.microsoft.com/3da1c3d2-5116-47c3-98e4-f29b33693c69">Sending Messages to the GINA</a>.

Before calling <b>WlxDisplayLockedNotice</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.




## -see-also




<a href="https://msdn.microsoft.com/2b56c037-aae6-4cb7-932f-15cf18c4444a">WlxDisplaySASNotice</a>



<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

