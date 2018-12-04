---
UID: NF:winwlx.WlxDisplaySASNotice
title: WlxDisplaySASNotice function
author: windows-sdk-content
description: Winlogon calls this function when no user is logged on.
old-location: security\wlxdisplaysasnotice.htm
tech.root: secauthn
ms.assetid: 2b56c037-aae6-4cb7-932f-15cf18c4444a
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: WlxDisplaySASNotice, WlxDisplaySASNotice function [Security], _gina_wlxdisplaysasnotice, security.wlxdisplaysasnotice, winwlx/WlxDisplaySASNotice
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
 - WlxDisplaySASNotice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WlxDisplaySASNotice function


## -description


<p class="CCE_Message">[The WlxDisplaySASNotice function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxDisplaySASNotice</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> calls this function when no user is logged on.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. This is the context value that the GINA returns when Winlogon calls 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> for this station.


## -returns



This function does not return a value.




## -remarks



Before calling <b>WlxDisplaySASNotice</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

