---
UID: NF:winwlx.WlxNegotiate
title: WlxNegotiate function
author: windows-sdk-content
description: The WlxNegotiate function must be implemented by a replacement GINA DLL. This is the first call made by Winlogon to the GINA DLL. WlxNegotiate allows the GINA to verify that it supports the installed version of Winlogon.
old-location: security\wlxnegotiate.htm
old-project: SecAuthN
ms.assetid: 9e7bab30-5cc6-4c55-82e4-d888e1af59ed
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: WlxNegotiate, WlxNegotiate function [Security], _gina_wlxnegotiate, security.wlxnegotiate, winwlx/WlxNegotiate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ICONINFOEXW, *PICONINFOEXW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winwlx.h
api_name:
-	WlxNegotiate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlxNegotiate function


## -description


<p class="CCE_Message">[The WlxNegotiate function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxNegotiate</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. This is the first call made by <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a> to the GINA DLL. <b>WlxNegotiate</b> allows the GINA to verify that it supports the installed version of Winlogon.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param dwWinlogonVersion

TBD


### -param pdwDllVersion [out]

Indicates which version of Winlogon the GINA supports. This version information is also used by Winlogon to determine which dispatch table is passed to the GINA in subsequent calls to 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>. This version cannot be greater than the version specified by <i>dwWinLogonVersion</i>.


#### - dwWinLogonVersion [in]

Specifies which version of Winlogon will be communicating with the GINA.


## -returns




					If the Winlogon version specified by <i>dwWinLogonVersion</i> is greater than or equal to the version returned in <i>pdwDllVersion</i>, the function returns <b>TRUE</b>. When <b>TRUE</b> is returned, Winlogon will continue to initialize.

If <i>dwWinLogonVersion</i> is less than <i>pdwDllVersion</i>, the function returns <b>FALSE</b>. When <b>FALSE</b> is returned, Winlogon will terminate and the system will not boot.




## -remarks



Before calling <b>WlxNegotiate</b>, <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a> sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

