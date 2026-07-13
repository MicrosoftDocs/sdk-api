---
UID: NF:contentpartner.IWMPContentContainer.GetType
title: IWMPContentContainer::GetType (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The GetType method retrieves the type of the content container.
helpviewer_keywords: ["GetType","GetType method [Windows Media Player]","GetType method [Windows Media Player]","IWMPContentContainer interface","IWMPContentContainer interface [Windows Media Player]","GetType method","IWMPContentContainer.GetType","IWMPContentContainer::GetType","IWMPContentContainerGetType","contentpartner/IWMPContentContainer::GetType","wmp.iwmpcontentcontainer_gettype"]
old-location: wmp\iwmpcontentcontainer_gettype.htm
tech.root: WMP
ms.assetid: 34c8ab5a-1f9f-4a71-9bf8-3b762d065da9
ms.date: 4/26/2023
ms.keywords: GetType, GetType method [Windows Media Player], GetType method [Windows Media Player],IWMPContentContainer interface, IWMPContentContainer interface [Windows Media Player],GetType method, IWMPContentContainer.GetType, IWMPContentContainer::GetType, IWMPContentContainerGetType, contentpartner/IWMPContentContainer::GetType, wmp.iwmpcontentcontainer_gettype
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
 - IWMPContentContainer::GetType
 - contentpartner/IWMPContentContainer::GetType
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
 - IWMPContentContainer.GetType
---

# IWMPContentContainer::GetType


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer">IWMPContentContainer Interface</a>