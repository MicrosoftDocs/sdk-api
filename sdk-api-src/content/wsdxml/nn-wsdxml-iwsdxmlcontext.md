---
UID: NN:wsdxml.IWSDXMLContext
title: IWSDXMLContext
author: windows-driver-content
description: Is a collection of namespaces and types used in a WSDAPI stack.
old-location: ncd\iwsdxmlcontext.htm
old-project: WsdApi
ms.assetid: 131fa170-4c19-4a7b-82e0-e9677b7f767a
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IWSDXMLContext, IWSDXMLContext interface, IWSDXMLContext interface,described, ncd.iwsdxmlcontext, wsdxml/IWSDXMLContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: RESPONSEBODY_SubscriptionEnd
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDXMLContext
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDXMLContext interface


## -description


Is a collection of namespaces and types used in a WSDAPI stack.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDXMLContext</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDXMLContext</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8815e01e-1879-48af-9011-84bb622259e9">AddNamespace</a>
</td>
<td align="left" width="63%">
Creates an object that represents an XML namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d480f868-46ab-4d9c-ae52-4e5ca5cb9fd9">AddNameToNamespace</a>
</td>
<td align="left" width="63%">
Creates an object that represents a name in an XML namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94ec94d1-e0d8-42cb-993f-6da9c8df1a47">SetNamespaces</a>
</td>
<td align="left" width="63%">
Associates custom namespaces with the XML context object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3bf56e1-42c6-4ecf-971f-2a6253fba0bc">SetTypes</a>
</td>
<td align="left" width="63%">
Associates custom message types with the XML context object. 

</td>
</tr>
</table> 


## -remarks



This interface is used by the XML parser and generator to store and access namespaces, names, and message schema information. Applications can call <a href="https://msdn.microsoft.com/8815e01e-1879-48af-9011-84bb622259e9">AddNamespace</a> and <a href="https://msdn.microsoft.com/d480f868-46ab-4d9c-ae52-4e5ca5cb9fd9">AddNameToNamespace</a> directly to add and access names in new or existing namespaces. Additionally, <a href="https://msdn.microsoft.com/76dffca8-bb84-4384-a9e8-120a4cf2acac">generated code</a> will call <a href="https://msdn.microsoft.com/94ec94d1-e0d8-42cb-993f-6da9c8df1a47">SetNamespaces</a> and <a href="https://msdn.microsoft.com/c3bf56e1-42c6-4ecf-971f-2a6253fba0bc">SetTypes</a> to ensure service layer data is properly set up in the XML context.



