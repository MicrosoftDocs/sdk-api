---
UID: NF:drt.DrtUpdateKey
title: DrtUpdateKey function
author: windows-sdk-content
description: DrtUpdateKey function updates the application data associated with a registered key.
old-location: p2p\drtupdatekey.htm
old-project: P2PSdk
ms.assetid: e7e65246-ebe0-4fdf-924c-8c19cfb1322e
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: DrtUpdateKey, DrtUpdateKey function [Distributed Routing Tables], drt/DrtUpdateKey, p2p.drtupdatekey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DRT_REGISTRATION_STATE, *PDRT_REGISTRATION_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	drt.dll
api_name:
-	DrtUpdateKey
product: Windows
targetos: Windows
req.lib: Drt.lib
req.dll: Drt.dll
req.irql: 
---

# DrtUpdateKey function


## -description


The <b>DrtUpdateKey</b> function updates the application data associated with a registered key.


## -parameters




### -param hKeyRegistration [in]

The DRT handle returned by the <a href="https://msdn.microsoft.com/9aa1ee16-648d-4769-a464-4659dea14dba">DrtRegisterKey</a> function specifying a registered key within the DRT instance.


### -param pAppData [in]

The new application data to associate with the key.


## -returns



This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li><i>pAppData</i> is <b>NULL</b></li>
<li>The value of <b>cb</b> in <i>pAppData</i> is less than 0.</li>
<li>The value of <b>cb</b> in <i>pAppData</i> is more than 5120.</li>
<li>The value of <b>pb</b> in <i>pAppData</i> is <b>NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>hKeyRegistration</i> is an invalid handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9aa1ee16-648d-4769-a464-4659dea14dba">DrtRegisterKey</a>



<a href="https://msdn.microsoft.com/cf8f877b-44a8-4153-bf02-0b0061bc53d2">DrtUnregisterKey</a>
 

 

