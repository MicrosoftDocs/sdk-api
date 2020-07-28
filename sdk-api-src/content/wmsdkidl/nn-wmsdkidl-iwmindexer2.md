---
UID: NN:wmsdkidl.IWMIndexer2
title: IWMIndexer2 (wmsdkidl.h)
description: The IWMIndexer2 interface enables you to change the settings of the indexer object to suit your needs.This interface is implemented as part of the indexer object.
helpviewer_keywords: ["IWMIndexer2","IWMIndexer2 interface [windows Media Format]","IWMIndexer2 interface [windows Media Format]","described","IWMIndexer2Interface","wmformat.iwmindexer2","wmsdkidl/IWMIndexer2"]
old-location: wmformat\iwmindexer2.htm
tech.root: wmformat
ms.assetid: ce900a2b-765b-46bb-87f4-bf9fe57d1cdb
ms.date: 12/05/2018
ms.keywords: IWMIndexer2, IWMIndexer2 interface [windows Media Format], IWMIndexer2 interface [windows Media Format],described, IWMIndexer2Interface, wmformat.iwmindexer2, wmsdkidl/IWMIndexer2
f1_keywords:
- wmsdkidl/IWMIndexer2
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmsdkidl.h
api_name:
- IWMIndexer2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMIndexer2 interface


## -description



The <b>IWMIndexer2</b> interface enables you to change the settings of the indexer object to suit your needs.

This interface is implemented as part of the indexer object. To obtain a pointer to <b>IWMIndexer2</b>, call the <b>QueryInterface</b> method of the <b>IWMIndexer</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMIndexer2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer">IWMIndexer</a>. <b>IWMIndexer2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMIndexer2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmindexer2-configure">Configure</a>
</td>
<td align="left" width="63%">
Enables custom configuration of the indexer object.

</td>
</tr>
</table> 

The following interface can be obtained by using the QueryInterface method of this interface.

<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer">IWMIndexer</a>
</td>
<td>IID_IWMIndexer</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer">IWMIndexer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/indexer-object">Indexer Object</a>
 

 

