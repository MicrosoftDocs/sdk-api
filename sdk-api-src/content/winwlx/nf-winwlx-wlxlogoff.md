---
UID: NF:winwlx.WlxLogoff
title: WlxLogoff function (winwlx.h)
author: windows-sdk-content
description: Winlogon calls this function to notify the GINA of a logoff operation on this workstation, allowing the GINA to perform any logoff operations that may be required.
old-location: security\wlxlogoff.htm
tech.root: SecAuthN
ms.assetid: bbeafd41-fe01-497d-8514-a6c088a11d73
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WlxLogoff, WlxLogoff function [Security], _gina_wlxlogoff, security.wlxlogoff, winwlx/WlxLogoff
ms.topic: function
f1_keywords: 
 - "winwlx/WlxLogoff"
dev_langs:
 - c++
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
 - WlxLogoff
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WlxLogoff function


## -description


<p class="CCE_Message">[The WlxLogoff function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxLogoff</b> function must be implemented by a replacement <a href="https://docs.microsoft.com/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="https://docs.microsoft.com/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function to notify the GINA of a logoff operation on this workstation, allowing the GINA to perform any logoff operations that may be required.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="https://docs.microsoft.com/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> for this station.


## -returns



This function does not return a value.




## -remarks



Before calling <b>WlxLogoff</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>
 

 

