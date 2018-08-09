---
UID: NF:contentpartner.IWMPContentPartnerCallback.AddListContents
title: IWMPContentPartnerCallback::AddListContents
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The AddListContents method adds a set of media items to a list.
old-location: wmp\iwmpcontentpartnercallback_addlistcontents.htm
old-project: WMP
ms.assetid: 22d28495-310e-4f3d-a0e3-8f6679c78c40
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: AddListContents, AddListContents method [Windows Media Player], AddListContents method [Windows Media Player],IWMPContentPartnerCallback interface, IWMPContentPartnerCallback interface [Windows Media Player],AddListContents method, IWMPContentPartnerCallback.AddListContents, IWMPContentPartnerCallback::AddListContents, IWMPContentPartnerCallbackAddListContents, contentpartner/IWMPContentPartnerCallback::AddListContents, wmp.iwmpcontentpartnercallback_addlistcontents
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
 - IWMPContentPartnerCallback.AddListContents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWMPContentPartnerCallback::AddListContents


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>AddListContents</b> method adds a set of media items to a list.




## -parameters




### -param dwListCookie [in]

A cookie that identifies a list retrieval session. Windows Media Player previously supplied this cookie to the content partner plug-in by calling <a href="https://msdn.microsoft.com/a48935ea-8275-4b68-a1ab-006a23c455ad">IWMPContentPartner::GetListContents</a>.


### -param cItems [in]

Count of items to be added to the list. This is the number of elements in the <i>prgItems</i> array.


### -param prgItems [in]

Pointer to an array of media item IDs. These are the IDs of the media items that are to be added to the list.


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




<a href="https://msdn.microsoft.com/3c66052b-2b82-44aa-868d-5d5a4501c457">IWMPContentPartnerCallback Interface</a>
 

 

