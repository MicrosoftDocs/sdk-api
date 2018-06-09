---
UID: NN:wbemdisp.ISWbemServicesEx
title: ISWbemServicesEx
author: windows-sdk-content
description: Extends the functionality of SWbemServices.
old-location: wmi\swbemservicesex.htm
old-project: WmiSdk
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemServicesEx, SWbemServicesEx, SWbemServicesEx object [Windows Management Instrumentation], SWbemServicesEx object [Windows Management Instrumentation],described, _hmm_swbemservicesex, wbemdisp/SWbemServicesEx, wmi.swbemservicesex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemServicesEx
 - ISWbemServicesEx
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServicesEx interface


## -description


The 
<b>SWbemServicesEx</b> object extends the functionality of 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>. The 
<a href="https://msdn.microsoft.com/1a9a718d-875d-4102-9d9d-3d10be162f58">Put</a> and 
<a href="https://msdn.microsoft.com/27da0c60-6dae-482d-a9bf-1aab016d3ae8">PutAsync</a> methods allow a class or an instance to be saved to multiple namespaces or to a different namespace than the one where an instance was created. This object cannot be created by the VBScript <a href="https://msdn.microsoft.com/en-us/library/xzysf6hc(v=vs.84).aspx">CreateObject</a>   call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemServicesEx</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>SWbemServicesEx</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a9a718d-875d-4102-9d9d-3d10be162f58">Put</a>
</td>
<td align="left" width="63%">
Saves the object to the namespace bound to the 
<b>SWbemServicesEx</b> object and returns an 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object that contains the path of the object to which the data was written.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27da0c60-6dae-482d-a9bf-1aab016d3ae8">PutAsync</a>
</td>
<td align="left" width="63%">
Saves an object asynchronously to a namespace.

</td>
</tr>
</table> 


## -remarks



The methods in this class can be called in either the semisynchronous mode or the asynchronous mode. For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.




## -see-also




<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>



<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>
 

 

