---
UID: NF:contentpartner.IWMPContentContainer.GetType
title: IWMPContentContainer::GetType (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The GetType method retrieves the type of the content container.
helpviewer_keywords: ["GetType","GetType method [Windows Media Player]","GetType method [Windows Media Player]","IWMPContentContainer interface","IWMPContentContainer interface [Windows Media Player]","GetType method","IWMPContentContainer.GetType","IWMPContentContainer::GetType","IWMPContentContainerGetType","contentpartner/IWMPContentContainer::GetType","wmp.iwmpcontentcontainer_gettype"]
old-location: wmp\iwmpcontentcontainer_gettype.htm
tech.root: WMP
ms.assetid: 34c8ab5a-1f9f-4a71-9bf8-3b762d065da9
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Windows Media Player], GetType method [Windows Media Player],IWMPContentContainer interface, IWMPContentContainer interface [Windows Media Player],GetType method, IWMPContentContainer.GetType, IWMPContentContainer::GetType, IWMPContentContainerGetType, contentpartner/IWMPContentContainer::GetType, wmp.iwmpcontentcontainer_gettype
f1_keywords:
- contentpartner/IWMPContentContainer.GetType
dev_langs:
- c++
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
- IWMPContentContainer.GetType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPContentContainer::GetType


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetType</b> method retrieves the type of the content container.




## -parameters




### -param pbstrType [out]

Pointer to a <b>BSTR</b> that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>g_szCPAlbumID</td>
<td>The content container contains an album.</td>
</tr>
<tr>
<td>g_szCPListID</td>
<td>The content container contains a list. A list, in this context, is a set of tracks that the online store offers as a bundle. The online store provides an ID and a price for the list as a whole.</td>
</tr>
<tr>
<td>g_szUnknownLocation</td>
<td>The content container contains a set of individual tracks.</td>
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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer">IWMPContentContainer Interface</a>
 

 

