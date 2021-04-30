---
UID: NF:contentpartner.IWMPContentContainerList.GetContainerCount
title: IWMPContentContainerList::GetContainerCount (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The GetContainerCount method retrieves the count of content containers in the container list.
helpviewer_keywords: ["GetContainerCount","GetContainerCount method [Windows Media Player]","GetContainerCount method [Windows Media Player]","IWMPContentContainerList interface","IWMPContentContainerList interface [Windows Media Player]","GetContainerCount method","IWMPContentContainerList.GetContainerCount","IWMPContentContainerList::GetContainerCount","IWMPContentContainerListGetContainerCount","contentpartner/IWMPContentContainerList::GetContainerCount","wmp.iwmpcontentcontainerlist_getcontainercount"]
old-location: wmp\iwmpcontentcontainerlist_getcontainercount.htm
tech.root: WMP
ms.assetid: e1ed4873-5d07-4a96-bd99-31ceeb423f98
ms.date: 12/05/2018
ms.keywords: GetContainerCount, GetContainerCount method [Windows Media Player], GetContainerCount method [Windows Media Player],IWMPContentContainerList interface, IWMPContentContainerList interface [Windows Media Player],GetContainerCount method, IWMPContentContainerList.GetContainerCount, IWMPContentContainerList::GetContainerCount, IWMPContentContainerListGetContainerCount, contentpartner/IWMPContentContainerList::GetContainerCount, wmp.iwmpcontentcontainerlist_getcontainercount
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPContentContainerList::GetContainerCount
 - contentpartner/IWMPContentContainerList::GetContainerCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentContainerList.GetContainerCount
---

# IWMPContentContainerList::GetContainerCount


## -description

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetContainerCount</b> method retrieves the count of content containers in the container list.

## -parameters

### -param pcContainer [out]

Address of a <b>ULONG</b> that receives the count.

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

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist">IWMPContentContainerList Interface</a>



<a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-getcontainer">IWMPContentContainerList::GetContainer</a>