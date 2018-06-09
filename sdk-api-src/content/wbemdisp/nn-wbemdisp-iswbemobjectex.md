---
UID: NN:wbemdisp.ISWbemObjectEx
title: ISWbemObjectEx
author: windows-sdk-content
description: Provides extended functionality for SWbemObject. Like SWbemObject, the methods of this extended object can be used by all WMI objects.
old-location: wmi\swbemobjectex.htm
old-project: WmiSdk
ms.assetid: 944d4cdc-ad35-4b53-b755-f10131a087fb
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemObjectEx, SWbemObjectEx, SWbemObjectEx object [Windows Management Instrumentation], SWbemObjectEx object [Windows Management Instrumentation],described, _hmm_swbemobjectex, wbemdisp/SWbemObjectEx, wmi.swbemobjectex
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
 - SWbemObjectEx
 - SetFromText_
 - ISWbemObjectEx
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObjectEx interface


## -description


The 
<b>SWbemObjectEx</b> object provides extended functionality for 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>. Like 
<b>SWbemObject</b>, the methods of this extended object can be used by all WMI objects. This object cannot be created by the VBScript <a href="https://msdn.microsoft.com/en-us/library/xzysf6hc(v=vs.84).aspx">CreateObject</a> call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemObjectEx</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>SWbemObjectEx</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98961d94-8360-4ed7-b1b1-20b4fca45d45">GetText_</a>
</td>
<td align="left" width="63%">
Returns a text file showing the contents of an object in XML.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6aeaa336-fb98-4eda-b746-fc958198d8ae">Refresh_</a>
</td>
<td align="left" width="63%">
Refreshes data in an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>SetFromText_</b></td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemObjectEx</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e95c325a-8851-4f55-a99d-4346d064e308">SystemProperties_</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
An 
<a href="https://msdn.microsoft.com/0edad17b-facc-4885-9ce4-561ca6f57a66">SWbemPropertySet</a> object that contains the collection of system properties that apply to the 
<b>SWbemObjectEx</b>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>



<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>



<a href="https://msdn.microsoft.com/0c97d16c-e6fc-431c-8d49-943f716a4284">WbemObjectTextFormatEnum</a>
 

 

