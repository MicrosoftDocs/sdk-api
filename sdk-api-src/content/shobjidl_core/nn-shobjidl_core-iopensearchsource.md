---
UID: NN:shobjidl_core.IOpenSearchSource
title: IOpenSearchSource (shobjidl_core.h)
description: Exposes a method to get search results from a custom client-side OpenSearch data source.
helpviewer_keywords: ["IOpenSearchSource","IOpenSearchSource interface [Windows Shell]","IOpenSearchSource interface [Windows Shell]","described","_shell_IOpenSearchSource","shell.IOpenSearchSource","shobjidl_core/IOpenSearchSource"]
old-location: shell\IOpenSearchSource.htm
tech.root: shell
ms.assetid: 8d5d376f-b59d-4420-a6be-d64459cb6aa3
ms.date: 12/05/2018
ms.keywords: IOpenSearchSource, IOpenSearchSource interface [Windows Shell], IOpenSearchSource interface [Windows Shell],described, _shell_IOpenSearchSource, shell.IOpenSearchSource, shobjidl_core/IOpenSearchSource
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpenSearchSource
 - shobjidl_core/IOpenSearchSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IOpenSearchSource
---

# IOpenSearchSource interface


## -description

Exposes a method to get search results from a custom client-side OpenSearch data source.

## -inheritance

The <b>IOpenSearchSource</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpenSearchSource</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement this interface when a server-side only solution will not work, such as the following: 
            

<ul>
<li>Remote indexes with authentication methods which Windows 7 search federation does not support, like forms-based authentication or other custom authentication methods.</li>
<li>High value public stores of vertical data which are not controlled by the developer (such as the Library of Congress or medical research databases) and which do not provide OpenSearch output support today but have public web API.</li>
<li>Proprietary enterprise data stores or indexes and legacy content management stores for which it might not be possible to implement a front end.</li>
</ul>
A client-side OpenSearch data source that sits in between the Windows OpenSearch provider and the external data source.

With a search connector (a .searchconnector-ms file), Windows Explorer calls your implementation with the query parameters. Your implementation returns results formatted in RSS or Atom format. That allows your implementation to provide custom authentication UI and connect to the data source using its proprietary API.
