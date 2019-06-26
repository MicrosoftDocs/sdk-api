---
UID: NF:contentpartner.IWMPContentContainer.GetContentID
title: IWMPContentContainer::GetContentID (contentpartner.h)
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentcontainer_getcontentid.htm
tech.root: WMP
ms.assetid: 95519f7e-aa78-4d66-87ba-71978d404412
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetContentID, GetContentID method [Windows Media Player], GetContentID method [Windows Media Player],IWMPContentContainer interface, IWMPContentContainer interface [Windows Media Player],GetContentID method, IWMPContentContainer.GetContentID, IWMPContentContainer::GetContentID, IWMPContentContainerGetContentID, contentpartner/IWMPContentContainer::GetContentID, wmp.iwmpcontentcontainer_getcontentid
ms.topic: method
f1_keywords: 
 - "contentpartner/IWMPContentContainer.GetContentID"
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
 - IWMPContentContainer.GetContentID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPContentContainer::GetContentID


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetContentID</b> method retrieves the ID of the media item at the specified index in the content container.




## -parameters




### -param idxContent [in]

Specifies the zero-based index of the media item in the container..


### -param pContentID [out]

Pointer to a <b>ULONG</b> that receives the ID of the media item.


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
 

 

