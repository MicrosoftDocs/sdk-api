---
UID: NN:wmp.IWMPErrorItem
title: IWMPErrorItem (wmp.h)
description: The IWMPErrorItem interface provides a way to access error information.
helpviewer_keywords: ["IWMPErrorItem","IWMPErrorItem interface [Windows Media Player]","IWMPErrorItem interface [Windows Media Player]","described","IWMPErrorItemInterface","wmp.iwmperroritem","wmp/IWMPErrorItem"]
old-location: wmp\iwmperroritem.htm
tech.root: WMP
ms.assetid: 4675eebf-80d7-4412-b3f1-ec54b977db31
ms.date: 12/05/2018
ms.keywords: IWMPErrorItem, IWMPErrorItem interface [Windows Media Player], IWMPErrorItem interface [Windows Media Player],described, IWMPErrorItemInterface, wmp.iwmperroritem, wmp/IWMPErrorItem
req.header: wmp.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPErrorItem
 - wmp/IWMPErrorItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPErrorItem
---

# IWMPErrorItem interface


## -description

The <b>IWMPErrorItem</b> interface provides a way to access error information.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPErrorItem</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPErrorItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPErrorItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmp/nf-wmp-iwmperroritem-get_customurl">get_customUrl</a>
</td>
<td align="left" width="63%">
Retrieves the URL of a website that displays specific information about codec download failure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmp/nf-wmp-iwmperroritem-get_errorcode">get_errorCode</a>
</td>
<td align="left" width="63%">
Retrieves the current error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmp/nf-wmp-iwmperroritem-get_errorcontext">get_errorContext</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the context of the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmp/nf-wmp-iwmperroritem-get_errordescription">get_errorDescription</a>
</td>
<td align="left" width="63%">
Retrieves a description of the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmp/nf-wmp-iwmperroritem-get_remedy">get_remedy</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPErrorItem</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nn-wmp-iwmperror">IWMPError</a>
</td>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmperror-get_item">get_item</a>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmperroritem2">IWMPErrorItem2 Interface</a>



<a href="/windows/desktop/WMP/interfaces">Interfaces</a>