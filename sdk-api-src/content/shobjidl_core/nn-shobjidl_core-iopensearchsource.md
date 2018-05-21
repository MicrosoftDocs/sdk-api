---
UID: NN:shobjidl_core.IOpenSearchSource
title: IOpenSearchSource
author: windows-driver-content
description: Exposes a method to get search results from a custom client-side OpenSearch data source.
old-location: shell\IOpenSearchSource.htm
old-project: shell
ms.assetid: 8d5d376f-b59d-4420-a6be-d64459cb6aa3
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IOpenSearchSource, IOpenSearchSource interface [Windows Shell], IOpenSearchSource interface [Windows Shell],described, _shell_IOpenSearchSource, shell.IOpenSearchSource, shobjidl_core/IOpenSearchSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IOpenSearchSource
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IOpenSearchSource interface


## -description


Exposes a method to get search results from a custom client-side OpenSearch data source.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpenSearchSource</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpenSearchSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpenSearchSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4fc16c04-cfb6-4f50-8325-bd3fc0b8f557">GetResults</a>
</td>
<td align="left" width="63%">
Returns search results, from an OpenSearch data source, formatted in RSS or Atom format.

</td>
</tr>
</table> 


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



