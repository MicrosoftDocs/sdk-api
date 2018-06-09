---
UID: NN:wbemdisp.ISWbemMethodSet
title: ISWbemMethodSet
author: windows-sdk-content
description: An SWbemMethodSet object is a collection of SWbemMethod objects. Items are retrieved using the Item method. For more information, see Accessing a Collection. This object cannot be created by the VBScript CreateObject call.
old-location: wmi\swbemmethodset.htm
old-project: WmiSdk
ms.assetid: 0ca2601f-ed40-472e-b4f2-eee750c8c8d1
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemMethodSet, SWbemMethodSet, SWbemMethodSet object [Windows Management Instrumentation], SWbemMethodSet object [Windows Management Instrumentation],described, _hmm_swbemmethodset, wbemdisp/SWbemMethodSet, wmi.swbemmethodset
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
 - SWbemMethodSet
 - ISWbemMethodSet
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemMethodSet interface


## -description


An 
<b>SWbemMethodSet</b> object is a collection of 
<a href="https://msdn.microsoft.com/461d5c41-4930-40cf-96e2-bc8cae335b60">SWbemMethod</a> objects. Items are retrieved using the 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a> method. For more information, see 
<a href="https://msdn.microsoft.com/c1ebe529-33cb-4158-923d-124d6328fc60">Accessing a Collection</a>. This object cannot be created by the VBScript <b>CreateObject</b> call.
<div class="alert"><b>Note</b>  In this version of the API, write access to method information is not supported. If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the MOF Compiler. Alternatively, use the WMI COM API.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemMethodSet</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>SWbemMethodSet</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
Retrieves an 
<a href="https://msdn.microsoft.com/461d5c41-4930-40cf-96e2-bc8cae335b60">SWbemMethod</a> object from the collection. This is the default automation method of this object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemMethodSet</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The number of items in the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>
 

 

