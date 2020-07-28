---
UID: NF:contentpartner.IWMPContentContainer.GetID
title: IWMPContentContainer::GetID (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The GetID method retrieves the ID of the album or list represented by the content container.
helpviewer_keywords: ["GetID","GetID method [Windows Media Player]","GetID method [Windows Media Player]","IWMPContentContainer interface","IWMPContentContainer interface [Windows Media Player]","GetID method","IWMPContentContainer.GetID","IWMPContentContainer::GetID","IWMPContentContainerGetID","contentpartner/IWMPContentContainer::GetID","wmp.iwmpcontentcontainer_getid"]
old-location: wmp\iwmpcontentcontainer_getid.htm
tech.root: WMP
ms.assetid: b2b4a5f8-ba53-4914-b8ef-ba9b7b87c52f
ms.date: 12/05/2018
ms.keywords: GetID, GetID method [Windows Media Player], GetID method [Windows Media Player],IWMPContentContainer interface, IWMPContentContainer interface [Windows Media Player],GetID method, IWMPContentContainer.GetID, IWMPContentContainer::GetID, IWMPContentContainerGetID, contentpartner/IWMPContentContainer::GetID, wmp.iwmpcontentcontainer_getid
f1_keywords:
- contentpartner/IWMPContentContainer.GetID
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
- IWMPContentContainer.GetID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPContentContainer::GetID


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetID</b> method retrieves the ID of the album or list represented by the content container.




## -parameters




### -param pContentID [out]

Pointer to a <b>ULONG</b> that receives the ID.


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



A list, in this context, is a set of tracks that the online store offers as a bundle. The online store provides an ID and a price for the list as a whole.

If the container does not represent an album or list, this method retrieves -1.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer">IWMPContentContainer Interface</a>
 

 

