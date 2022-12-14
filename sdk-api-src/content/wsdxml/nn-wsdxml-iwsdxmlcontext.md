---
UID: NN:wsdxml.IWSDXMLContext
title: IWSDXMLContext (wsdxml.h)
description: Is a collection of namespaces and types used in a WSDAPI stack.
helpviewer_keywords: ["IWSDXMLContext","IWSDXMLContext interface","IWSDXMLContext interface","described","ncd.iwsdxmlcontext","wsdxml/IWSDXMLContext"]
old-location: ncd\iwsdxmlcontext.htm
tech.root: ncd
ms.assetid: 131fa170-4c19-4a7b-82e0-e9677b7f767a
ms.date: 12/05/2018
ms.keywords: IWSDXMLContext, IWSDXMLContext interface, IWSDXMLContext interface,described, ncd.iwsdxmlcontext, wsdxml/IWSDXMLContext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDXMLContext
 - wsdxml/IWSDXMLContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDXMLContext
---

# IWSDXMLContext interface


## -description

Is a collection of namespaces and types used in a WSDAPI stack.

## -inheritance

The <b>IWSDXMLContext</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDXMLContext</b> also has these types of members:

## -remarks

This interface is used by the XML parser and generator to store and access namespaces, names, and message schema information. Applications can call <a href="/windows/desktop/api/wsdxml/nf-wsdxml-iwsdxmlcontext-addnamespace">AddNamespace</a> and <a href="/windows/desktop/api/wsdxml/nf-wsdxml-iwsdxmlcontext-addnametonamespace">AddNameToNamespace</a> directly to add and access names in new or existing namespaces. Additionally, <a href="/windows/desktop/WsdApi/web-services-for-devices-code-generator">generated code</a> will call <a href="/windows/desktop/api/wsdxml/nf-wsdxml-iwsdxmlcontext-setnamespaces">SetNamespaces</a> and <a href="/windows/desktop/api/wsdxml/nf-wsdxml-iwsdxmlcontext-settypes">SetTypes</a> to ensure service layer data is properly set up in the XML context.
