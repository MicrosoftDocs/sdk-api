---
UID: NF:contentpartner.IWMPContentContainer.GetContentCount
title: IWMPContentContainer::GetContentCount (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["GetContentCount","GetContentCount method [Windows Media Player]","GetContentCount method [Windows Media Player]","IWMPContentContainer interface","IWMPContentContainer interface [Windows Media Player]","GetContentCount method","IWMPContentContainer.GetContentCount","IWMPContentContainer::GetContentCount","IWMPContentContainerGetContentCount","contentpartner/IWMPContentContainer::GetContentCount","wmp.iwmpcontentcontainer_getcontentcount"]
old-location: wmp\iwmpcontentcontainer_getcontentcount.htm
tech.root: WMP
ms.assetid: 0a12f6b3-c253-4d07-aa5e-556faa6fbccb
ms.date: 12/05/2018
ms.keywords: GetContentCount, GetContentCount method [Windows Media Player], GetContentCount method [Windows Media Player],IWMPContentContainer interface, IWMPContentContainer interface [Windows Media Player],GetContentCount method, IWMPContentContainer.GetContentCount, IWMPContentContainer::GetContentCount, IWMPContentContainerGetContentCount, contentpartner/IWMPContentContainer::GetContentCount, wmp.iwmpcontentcontainer_getcontentcount
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
 - IWMPContentContainer::GetContentCount
 - contentpartner/IWMPContentContainer::GetContentCount
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
 - IWMPContentContainer.GetContentCount
---

# IWMPContentContainer::GetContentCount


## -description

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetContentCount</b> method retrieves the count of digital media content items in the container.

## -parameters

### -param pcContent [out]

Pointer to a <b>ULONG</b> that receives the count.

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

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer">IWMPContentContainer Interface</a>