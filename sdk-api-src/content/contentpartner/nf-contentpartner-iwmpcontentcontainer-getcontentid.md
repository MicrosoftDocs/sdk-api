---
UID: NF:contentpartner.IWMPContentContainer.GetContentID
title: IWMPContentContainer::GetContentID (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["GetContentID","GetContentID method [Windows Media Player]","GetContentID method [Windows Media Player]","IWMPContentContainer interface","IWMPContentContainer interface [Windows Media Player]","GetContentID method","IWMPContentContainer.GetContentID","IWMPContentContainer::GetContentID","IWMPContentContainerGetContentID","contentpartner/IWMPContentContainer::GetContentID","wmp.iwmpcontentcontainer_getcontentid"]
old-location: wmp\iwmpcontentcontainer_getcontentid.htm
tech.root: WMP
ms.assetid: 95519f7e-aa78-4d66-87ba-71978d404412
ms.date: 4/26/2023
ms.keywords: GetContentID, GetContentID method [Windows Media Player], GetContentID method [Windows Media Player],IWMPContentContainer interface, IWMPContentContainer interface [Windows Media Player],GetContentID method, IWMPContentContainer.GetContentID, IWMPContentContainer::GetContentID, IWMPContentContainerGetContentID, contentpartner/IWMPContentContainer::GetContentID, wmp.iwmpcontentcontainer_getcontentid
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
 - IWMPContentContainer::GetContentID
 - contentpartner/IWMPContentContainer::GetContentID
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
 - IWMPContentContainer.GetContentID
---

# IWMPContentContainer::GetContentID


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer">IWMPContentContainer Interface</a>