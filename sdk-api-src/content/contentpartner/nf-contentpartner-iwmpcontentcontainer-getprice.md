---
UID: NF:contentpartner.IWMPContentContainer.GetPrice
title: IWMPContentContainer::GetPrice
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentcontainer_getprice.htm
old-project: WMP
ms.assetid: 2ed27b14-9567-4943-81c3-282316ce1605
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetPrice, GetPrice method [Windows Media Player], GetPrice method [Windows Media Player],IWMPContentContainer interface, IWMPContentContainer interface [Windows Media Player],GetPrice method, IWMPContentContainer.GetPrice, IWMPContentContainer::GetPrice, IWMPContentContainerGetPrice, contentpartner/IWMPContentContainer::GetPrice, wmp.iwmpcontentcontainer_getprice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
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
tech.root: 
req.typenames: WMPTransactionType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentContainer.GetPrice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWMPContentContainer::GetPrice


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetPrice</b> method retrieves the total price of the album or list represented by the content container.




## -parameters




### -param pbstrPrice [out]

Pointer to a <b>BSTR</b> that receives the price or one of the following constants.

<table>
<tr>
<th>String
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>g_szContentPrice_Unknown</td>
<td>The price of the content is unknown.</td>
</tr>
<tr>
<td>g_szContentPrice_CannotBuy</td>
<td>The content cannot be purchased.</td>
</tr>
<tr>
<td>g_szContentPrice_Free</td>
<td>The content is free.</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The format of the string returned in <i>pbstrPrice</i> is known only to the online store. Windows Media Player displays, but does not interpret, price strings. For more information about how Windows Media Player and the content partner plug-in exchange price information, see <a href="https://msdn.microsoft.com/df4a3152-f9e3-4a97-b021-6d5e8de9c184">Purchasing Media Content</a>.

A list, in this context, is a set of tracks that the online store offers as a bundle. The online store provides an ID and a price for the list as a whole.

If the content container does not represent an album or list, this method retrieves g_szContentPrice_Unknown.




## -see-also




<a href="https://msdn.microsoft.com/32a68af3-9270-4ac1-b133-a2770220dfcb">IWMPContentContainer Interface</a>
 

 

