---
UID: NN:contentpartner.IWMPContentContainer
title: IWMPContentContainer (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentcontainer.htm
tech.root: WMP
ms.assetid: 32a68af3-9270-4ac1-b133-a2770220dfcb
ms.date: 12/05/2018
ms.keywords: IWMPContentContainer, IWMPContentContainer interface [Windows Media Player], IWMPContentContainer interface [Windows Media Player],described, IWMPContentContainerInterface, contentpartner/IWMPContentContainer, wmp.iwmpcontentcontainer
f1_keywords:
- contentpartner/IWMPContentContainer
dev_langs:
- c++
req.header: contentpartner.h
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
- contentpartner.h
api_name:
- IWMPContentContainer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPContentContainer interface


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPContentContainer</b> interface represents a container for information about digital media content in an online store.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPContentContainer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPContentContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPContentContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainer-getcontentcount">GetContentCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of digital media content items in the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainer-getcontentid">GetContentID</a>
</td>
<td align="left" width="63%">
Retrieves the ID of the media item at the specified index in the content container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainer-getcontentprice">GetContentPrice</a>
</td>
<td align="left" width="63%">
Retrieves the price of the media item at the specified index in the content container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainer-getid">GetID</a>
</td>
<td align="left" width="63%">
Retrieves the ID of the album or list represented by the content container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainer-getprice">GetPrice</a>
</td>
<td align="left" width="63%">
Retrieves the total price of the album or list represented by the content container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainer-gettype">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the type of the content container.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/reference-for-type-1-online-stores">Reference for Type 1 Online Stores</a>
 

 

