---
UID: NN:contentpartner.IWMPContentContainer
title: IWMPContentContainer
author: windows-driver-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentcontainer.htm
old-project: WMP
ms.assetid: 32a68af3-9270-4ac1-b133-a2770220dfcb
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPContentContainer, IWMPContentContainer interface [Windows Media Player], IWMPContentContainer interface [Windows Media Player],described, IWMPContentContainerInterface, contentpartner/IWMPContentContainer, wmp.iwmpcontentcontainer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: WMPTransactionType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	contentpartner.h
api_name:
-	IWMPContentContainer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWMPContentContainer interface


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPContentContainer</b> interface represents a container for information about digital media content in an online store.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPContentContainer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPContentContainer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0a12f6b3-c253-4d07-aa5e-556faa6fbccb">GetContentCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of digital media content items in the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95519f7e-aa78-4d66-87ba-71978d404412">GetContentID</a>
</td>
<td align="left" width="63%">
Retrieves the ID of the media item at the specified index in the content container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae0a9f37-2337-419e-b912-2102e8eb2a39">GetContentPrice</a>
</td>
<td align="left" width="63%">
Retrieves the price of the media item at the specified index in the content container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546827">GetID</a>
</td>
<td align="left" width="63%">
Retrieves the ID of the album or list represented by the content container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ed27b14-9567-4943-81c3-282316ce1605">GetPrice</a>
</td>
<td align="left" width="63%">
Retrieves the total price of the album or list represented by the content container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the type of the content container.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e6f45a50-029e-4347-9b25-10e9e32a56eb">Reference for Type 1 Online Stores</a>
 

 

