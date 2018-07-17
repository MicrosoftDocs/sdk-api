---
UID: NN:wsmandisp.IWSManResourceLocator
title: IWSManResourceLocator
author: windows-sdk-content
description: Supplies the path to a resource. You can use an IWSManResourceLocator object instead of a resource URI in IWSManSession object operations such as IWSManSession.Get, IWSManSession.Put, or IWSManSession.Enumerate.
old-location: winrm\iwsmanresourcelocator.htm
old-project: winrm
ms.assetid: 7b3dcb53-d02c-4ba6-973d-1493ba442387
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IWSManResourceLocator, IWSManResourceLocator interface [Windows Remote Management], IWSManResourceLocator interface [Windows Remote Management],described, winrm.iwsmanresourcelocator, wsmandisp/IWSManResourceLocator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSManProxyAuthenticationFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManResourceLocator
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManResourceLocator interface


## -description


 Supplies the path to a resource. You can use an <b>IWSManResourceLocator</b> object instead of a <a href="https://msdn.microsoft.com/library/Aa384465(v=VS.85).aspx">resource URI</a> in <a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a> object operations such as <a href="https://msdn.microsoft.com/873242fd-9da3-42f4-a18e-258fedba77ec">IWSManSession.Get</a>, <a href="https://msdn.microsoft.com/f121d9ce-6aa3-45e3-b0ba-67b19c2f5665">IWSManSession.Put</a>, or <a href="https://msdn.microsoft.com/ed8ad3ad-d033-45cb-b681-995c5f73b12e">IWSManSession.Enumerate</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSManResourceLocator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSManResourceLocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWSManResourceLocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6709cb7-35a1-41b6-981e-13d3f1bf9816">AddOption</a>
</td>
<td align="left" width="63%">
Adds additional data required to process the request. For example, some WMI providers may require an <a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> or <a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object with provider-specific information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f6c1169-8e2a-4919-9a1a-856dbe41a9ce">AddSelector</a>
</td>
<td align="left" width="63%">
Adds a <a href="https://msdn.microsoft.com/library/Aa384465(v=VS.85).aspx">selector</a> to the <b>IWSManResourceLocator</b> object. The selector specifies a particular instance of a <i>resource</i>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c71948d-2321-41b5-b961-c4a514830b26">ClearOptions</a>
</td>
<td align="left" width="63%">
Removes any <a href="https://msdn.microsoft.com/library/windows/hardware/dn965779">options</a> from the <b>IWSManResourceLocator</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fccd0cd4-465b-454c-a300-ab50c25d6afe">ClearSelectors</a>
</td>
<td align="left" width="63%">
Removes all the <a href="https://msdn.microsoft.com/library/Aa384465(v=VS.85).aspx">selectors</a> from an <b>IWSManResourceLocator</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSManResourceLocator</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/040333f5-32b0-4ec8-8deb-da9fcb2ea46b">Error</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an XML representation of additional error information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/eb458fc4-ddcc-42a2-8dd3-05498e035de2">FragmentDialect</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the language dialect for a <a href="https://msdn.microsoft.com/library/Aa384465(v=VS.85).aspx">resource</a> <a href="https://msdn.microsoft.com/library/Aa384465(v=VS.85).aspx">fragment</a> <i>dialect</i> when <b>IWSManResourceLocator</b> is used in <a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a> object methods such as <a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>, <a href="https://msdn.microsoft.com/1224dab8-82d1-4416-8c21-e84fdda15deb">Put</a>, or <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">Enumerate</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c20c0c03-4fe4-417f-95e0-0a9b34b3c1ee">FragmentPath Property</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the path for a <a href="https://msdn.microsoft.com/library/Aa384465(v=VS.85).aspx">resource</a> <a href="https://msdn.microsoft.com/library/Aa384465(v=VS.85).aspx">fragment</a> or property when an instance of <b>IWSManResourceLocator</b> is used in <a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a> methods such as <a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>, <a href="https://msdn.microsoft.com/1224dab8-82d1-4416-8c21-e84fdda15deb">Put</a>, or <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">Enumerate</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fff64708-faef-4f61-b569-17d9ff52dc64">MustUnderstandOptions Property</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the <b>MustUnderstandOptions</b> value for the <b>IWSManResourceLocator</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8ae490a3-ae6d-46e4-9a51-5a1e9c80cf77">ResourceURI Property</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/Aa384465(v=VS.85).aspx">resource URI</a> of the requested resource. This property can contain only the path, not a query string for specific instances.

</td>
</tr>
</table> 


## -remarks



The corresponding scripting object is <a href="https://msdn.microsoft.com/0904b7eb-d4ce-46a7-bf58-452e7c0d41e9">ResourceLocator</a>.




## -see-also




<a href="https://msdn.microsoft.com/0904b7eb-d4ce-46a7-bf58-452e7c0d41e9">ResourceLocator</a>



<a href="https://msdn.microsoft.com/c996f074-f14b-4edd-80b7-8f4de4cbabb0">Windows Remote Management Reference</a>
 

 

