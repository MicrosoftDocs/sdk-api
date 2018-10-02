---
UID: NF:winwlx.WlxLogoff
title: WlxLogoff function
author: windows-sdk-content
description: Winlogon calls this function to notify the GINA of a logoff operation on this workstation, allowing the GINA to perform any logoff operations that may be required.
old-location: security\wlxlogoff.htm
tech.root: secauthn
ms.assetid: bbeafd41-fe01-497d-8514-a6c088a11d73
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: WlxLogoff, WlxLogoff function [Security], _gina_wlxlogoff, security.wlxlogoff, winwlx/WlxLogoff
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
 - WlxLogoff
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WlxLogoff function


## -description


<p class="CCE_Message">[The WlxLogoff function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxLogoff</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> calls this function to notify the GINA of a logoff operation on this workstation, allowing the GINA to perform any logoff operations that may be required.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> for this station.


## -returns



This function does not return a value.




## -remarks



Before calling <b>WlxLogoff</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

