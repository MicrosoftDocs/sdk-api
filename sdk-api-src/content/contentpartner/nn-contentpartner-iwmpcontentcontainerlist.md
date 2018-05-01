---
UID: NN:contentpartner.IWMPContentContainerList
title: IWMPContentContainerList
author: windows-driver-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentcontainerlist.htm
old-project: WMP
ms.assetid: a8fd239b-2a53-4db4-8a82-a7c510d215bc
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPContentContainerList, IWMPContentContainerList interface [Windows Media Player], IWMPContentContainerList interface [Windows Media Player], described, IWMPContentContainerListInterface, contentpartner/IWMPContentContainerList, wmp.iwmpcontentcontainerlist
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
-	IWMPContentContainerList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWMPContentContainerList interface


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPContentContainerList</b> interface represents a list of one or more content containers. Content containers are represented by the <a href="https://msdn.microsoft.com/32a68af3-9270-4ac1-b133-a2770220dfcb">IWMPContentContainer</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPContentContainerList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPContentContainerList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPContentContainerList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8922aeed-0598-4dc8-86ac-e113697fcea9">GetContainer</a>
</td>
<td align="left" width="63%">
Retrieves the content container at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1ed4873-5d07-4a96-bd99-31ceeb423f98">GetContainerCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of content containers in the container list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8712d134-9dd3-4964-ae53-f63c8b69818d">GetTransactionType</a>
</td>
<td align="left" width="63%">
Retrieves the type of the current transaction.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e6f45a50-029e-4347-9b25-10e9e32a56eb">Reference for Type 1 Online Stores</a>
 

 

