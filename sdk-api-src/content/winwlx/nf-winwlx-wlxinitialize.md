---
UID: NF:winwlx.WlxInitialize
title: WlxInitialize function
author: windows-driver-content
description: Winlogon calls this function once for each window station present on the computer. Currently, the operating system supports one window station per workstation.
old-location: security\wlxinitialize.htm
old-project: SecAuthN
ms.assetid: db03f2b3-0719-40be-8a42-04ab7110f711
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: WLX_DISPATCH_VERSION_1_0, WLX_DISPATCH_VERSION_1_1, WLX_DISPATCH_VERSION_1_2, WLX_DISPATCH_VERSION_1_3, WLX_DISPATCH_VERSION_1_4, WlxInitialize, WlxInitialize function [Security], _gina_wlxinitialize, security.wlxinitialize, winwlx/WlxInitialize
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
-	WlxInitialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlxInitialize function


## -description


<p class="CCE_Message">[The WlxInitialize function is no longer available for use as of Windows Server 2008 and Windows Vista.]


			The <b>WlxInitialize</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a> calls this function once for each window station present on the computer. Currently, the operating system supports one window station per workstation.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>The <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">context</a> returned by this function will be passed back to the GINA in all subsequent calls.


## -parameters




### -param lpWinsta [in]

A pointer to the name of the window station being initialized.


### -param hWlx [in]

A handle to Winlogon. The GINA must supply this handle in all calls to Winlogon support functions that involve this window station.


### -param pvReserved [in]

This parameter is reserved for future use and must be set to <b>NULL</b>.


### -param pWinlogonFunctions [in]

A pointer to a Winlogon support function dispatch table. The contents of the table depend on the GINA DLL version returned by the 
<a href="https://msdn.microsoft.com/9e7bab30-5cc6-4c55-82e4-d888e1af59ed">WlxNegotiate</a> call. This table does not change, which allows the GINA DLL to reference the table without copying it. If the GINA DLL needs to make a copy of the table, it should call <a href="https://msdn.microsoft.com/724477d4-ec56-44bd-801e-23c225bafd03">WlxGetOption</a> and supply WLX_OPTION_DISPATCH_TABLE_SIZE for the <b>Option</b> parameter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLX_DISPATCH_VERSION_1_4"></a><a id="wlx_dispatch_version_1_4"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/b2d0c936-5430-48ed-b808-92209b909406">WLX_DISPATCH_VERSION_1_4</a></b></dt>
</dl>
</td>
<td width="60%">
Winlogon dispatch table - version 1.4

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_DISPATCH_VERSION_1_3"></a><a id="wlx_dispatch_version_1_3"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/47e343b8-ee54-45de-98c6-0ec75b45aa90">WLX_DISPATCH_VERSION_1_3</a></b></dt>
</dl>
</td>
<td width="60%">

								Winlogon dispatch table - version 1.3

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_DISPATCH_VERSION_1_2"></a><a id="wlx_dispatch_version_1_2"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/d6b3444f-ee74-40b3-a729-304c8e50195b">WLX_DISPATCH_VERSION_1_2</a></b></dt>
</dl>
</td>
<td width="60%">

								Winlogon dispatch table - version 1.2

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_DISPATCH_VERSION_1_1"></a><a id="wlx_dispatch_version_1_1"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/b76f4417-4414-4912-924f-3afef7156f08">WLX_DISPATCH_VERSION_1_1</a></b></dt>
</dl>
</td>
<td width="60%">

								Winlogondispatch table - version 1.1

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_DISPATCH_VERSION_1_0"></a><a id="wlx_dispatch_version_1_0"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/13b08978-5112-44d8-ae41-207e0040eb73">WLX_DISPATCH_VERSION_1_0</a></b></dt>
</dl>
</td>
<td width="60%">

								Winlogon dispatch table - version 1.0

</td>
</tr>
</table>
 


### -param pWlxContext [out]

A pointer to a pointer to a <b>VOID</b> that will contain the address of the GINA context for this window station. This context is passed in all subsequent calls to the GINA from Winlogon. The GINA DLL manages any memory used by the context. The context pointer can be changed later by calling the <a href="https://msdn.microsoft.com/59f775dd-b3ed-4a57-bec7-fa6ddf267401">WlxSetOption</a> function with WLX_OPTION_CONTEXT_POINTER.


## -returns




					If the function successfully initializes the GINA DLL, the function returns <b>TRUE</b>.

If the function fails, or if the GINA DLL was not initialized, the function returns <b>FALSE</b>. Winlogon will terminate, and the system will not boot.




## -remarks



<b>WlxInitialize</b> is called once for each window station present on the computer.

Currently only a single window station called Winsta0 is supported.

Before calling <b>WlxInitialize</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.




## -see-also




<a href="https://msdn.microsoft.com/9e7bab30-5cc6-4c55-82e4-d888e1af59ed">WlxNegotiate</a>
 

 

