---
UID: NN:wsdxml.IWSDXMLContext
title: IWSDXMLContext (wsdxml.h)
author: windows-sdk-content
description: Is a collection of namespaces and types used in a WSDAPI stack.
old-location: ncd\iwsdxmlcontext.htm
tech.root: WsdApi
ms.assetid: 131fa170-4c19-4a7b-82e0-e9677b7f767a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDXMLContext, IWSDXMLContext interface, IWSDXMLContext interface,described, ncd.iwsdxmlcontext, wsdxml/IWSDXMLContext
ms.topic: interface
f1_keywords: 
 - "wsdxml/IWSDXMLContext"
req.header: wsdxml.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdXml.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDXMLContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDXMLContext interface


## -description


Is a collection of namespaces and types used in a WSDAPI stack.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDXMLContext</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDXMLContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDXMLContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdxml/nf-wsdxml-iwsdxmlcontext-addnamespace">AddNamespace</a>
</td>
<td align="left" width="63%">
Creates an object that represents an XML namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdxml/nf-wsdxml-iwsdxmlcontext-addnametonamespace">AddNameToNamespace</a>
</td>
<td align="left" width="63%">
Creates an object that represents a name in an XML namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdxml/nf-wsdxml-iwsdxmlcontext-setnamespaces">SetNamespaces</a>
</td>
<td align="left" width="63%">
Associates custom namespaces with the XML context object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdxml/nf-wsdxml-iwsdxmlcontext-settypes">SetTypes</a>
</td>
<td align="left" width="63%">
Associates custom message types with the XML context object. 

</td>
</tr>
</table> 


## -remarks



This interface is used by the XML parser and generator to store and access namespaces, names, and message schema information. Applications can call <a href="https://docs.microsoft.com/windows/desktop/api/wsdxml/nf-wsdxml-iwsdxmlcontext-addnamespace">AddNamespace</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wsdxml/nf-wsdxml-iwsdxmlcontext-addnametonamespace">AddNameToNamespace</a> directly to add and access names in new or existing namespaces. Additionally, <a href="https://docs.microsoft.com/windows/desktop/WsdApi/web-services-for-devices-code-generator">generated code</a> will call <a href="https://docs.microsoft.com/windows/desktop/api/wsdxml/nf-wsdxml-iwsdxmlcontext-setnamespaces">SetNamespaces</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wsdxml/nf-wsdxml-iwsdxmlcontext-settypes">SetTypes</a> to ensure service layer data is properly set up in the XML context.



