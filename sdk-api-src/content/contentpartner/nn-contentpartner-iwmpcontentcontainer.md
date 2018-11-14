---
UID: NN:contentpartner.IWMPContentContainer
title: IWMPContentContainer
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentcontainer.htm
tech.root: WMP
ms.assetid: 32a68af3-9270-4ac1-b133-a2770220dfcb
ms.author: windowssdkdev
ms.date: 09/27/2018
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPContentContainer interface


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPContentContainer</b> interface represents a container for information about digital media content in an online store.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPContentContainer</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IWMPContentContainer</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd563135(v=VS.85).aspx">GetContentCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of digital media content items in the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563136(v=VS.85).aspx">GetContentID</a>
</td>
<td align="left" width="63%">
Retrieves the ID of the media item at the specified index in the content container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563137(v=VS.85).aspx">GetContentPrice</a>
</td>
<td align="left" width="63%">
Retrieves the price of the media item at the specified index in the content container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563138(v=VS.85).aspx">GetID</a>
</td>
<td align="left" width="63%">
Retrieves the ID of the album or list represented by the content container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563139(v=VS.85).aspx">GetPrice</a>
</td>
<td align="left" width="63%">
Retrieves the total price of the album or list represented by the content container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563140(v=VS.85).aspx">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the type of the content container.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd564243(v=VS.85).aspx">Reference for Type 1 Online Stores</a>
 

 

