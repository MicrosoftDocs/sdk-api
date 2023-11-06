---
UID: NF:contentpartner.IWMPContentContainer.GetContentCount
title: IWMPContentContainer::GetContentCount (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["GetContentCount","GetContentCount method [Windows Media Player]","GetContentCount method [Windows Media Player]","IWMPContentContainer interface","IWMPContentContainer interface [Windows Media Player]","GetContentCount method","IWMPContentContainer.GetContentCount","IWMPContentContainer::GetContentCount","IWMPContentContainerGetContentCount","contentpartner/IWMPContentContainer::GetContentCount","wmp.iwmpcontentcontainer_getcontentcount"]
old-location: wmp\iwmpcontentcontainer_getcontentcount.htm
tech.root: WMP
ms.assetid: 0a12f6b3-c253-4d07-aa5e-556faa6fbccb
ms.date: 4/26/2023
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

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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