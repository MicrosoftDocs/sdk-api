---
UID: NN:wsmandisp.IWSManResourceLocator
title: IWSManResourceLocator (wsmandisp.h)
description: Supplies the path to a resource. You can use an IWSManResourceLocator object instead of a resource URI in IWSManSession object operations such as IWSManSession.Get, IWSManSession.Put, or IWSManSession.Enumerate.helpviewer_keywords: ["IWSManResourceLocator","IWSManResourceLocator interface [Windows Remote Management]","IWSManResourceLocator interface [Windows Remote Management]","described","winrm.iwsmanresourcelocator","wsmandisp/IWSManResourceLocator"]
old-location: winrm\iwsmanresourcelocator.htm
tech.root: winrm
ms.assetid: 7b3dcb53-d02c-4ba6-973d-1493ba442387
ms.date: 12/05/2018
ms.keywords: IWSManResourceLocator, IWSManResourceLocator interface [Windows Remote Management], IWSManResourceLocator interface [Windows Remote Management],described, winrm.iwsmanresourcelocator, wsmandisp/IWSManResourceLocator
f1_keywords:
- wsmandisp/IWSManResourceLocator
dev_langs:
- c++
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
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- WSMAuto.dll
api_name:
- IWSManResourceLocator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSManResourceLocator interface


## -description


 Supplies the path to a resource. You can use an <b>IWSManResourceLocator</b> object instead of a <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">resource URI</a> in <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a> object operations such as <a href="https://docs.microsoft.com/windows/desktop/WinRM/session-get">IWSManSession.Get</a>, <a href="https://docs.microsoft.com/windows/desktop/WinRM/session-put">IWSManSession.Put</a>, or <a href="https://docs.microsoft.com/windows/desktop/WinRM/session-enumerate">IWSManSession.Enumerate</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSManResourceLocator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSManResourceLocator</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanresourcelocator-addoption">AddOption</a>
</td>
<td align="left" width="63%">
Adds additional data required to process the request. For example, some WMI providers may require an <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> or <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/swbemnamedvalueset">SWbemNamedValueSet</a> object with provider-specific information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanresourcelocator-addselector">AddSelector</a>
</td>
<td align="left" width="63%">
Adds a <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">selector</a> to the <b>IWSManResourceLocator</b> object. The selector specifies a particular instance of a <i>resource</i>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanresourcelocator-clearoptions">ClearOptions</a>
</td>
<td align="left" width="63%">
Removes any <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">options</a> from the <b>IWSManResourceLocator</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanresourcelocator-clearselectors">ClearSelectors</a>
</td>
<td align="left" width="63%">
Removes all the <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">selectors</a> from an <b>IWSManResourceLocator</b> object.

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

<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanresourcelocator-get_error">Error</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect">FragmentDialect</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the language dialect for a <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">resource</a> <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">fragment</a> <i>dialect</i> when <b>IWSManResourceLocator</b> is used in <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a> object methods such as <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get">Get</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-put">Put</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">Enumerate</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentpath">FragmentPath Property</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the path for a <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">resource</a> <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">fragment</a> or property when an instance of <b>IWSManResourceLocator</b> is used in <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a> methods such as <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get">Get</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-put">Put</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">Enumerate</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanresourcelocator-get_mustunderstandoptions">MustUnderstandOptions Property</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri">ResourceURI Property</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">resource URI</a> of the requested resource. This property can contain only the path, not a query string for specific instances.

</td>
</tr>
</table> 


## -remarks



The corresponding scripting object is <a href="https://docs.microsoft.com/windows/desktop/WinRM/resourcelocator">ResourceLocator</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinRM/resourcelocator">ResourceLocator</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-reference">Windows Remote Management Reference</a>
 

 

