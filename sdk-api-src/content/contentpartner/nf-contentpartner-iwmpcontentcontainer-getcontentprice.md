---
UID: NF:contentpartner.IWMPContentContainer.GetContentPrice
title: IWMPContentContainer::GetContentPrice (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["GetContentPrice","GetContentPrice method [Windows Media Player]","GetContentPrice method [Windows Media Player]","IWMPContentContainer interface","IWMPContentContainer interface [Windows Media Player]","GetContentPrice method","IWMPContentContainer.GetContentPrice","IWMPContentContainer::GetContentPrice","IWMPContentContainerGetContentPrice","contentpartner/IWMPContentContainer::GetContentPrice","wmp.iwmpcontentcontainer_getcontentprice"]
old-location: wmp\iwmpcontentcontainer_getcontentprice.htm
tech.root: WMP
ms.assetid: ae0a9f37-2337-419e-b912-2102e8eb2a39
ms.date: 4/26/2023
ms.keywords: GetContentPrice, GetContentPrice method [Windows Media Player], GetContentPrice method [Windows Media Player],IWMPContentContainer interface, IWMPContentContainer interface [Windows Media Player],GetContentPrice method, IWMPContentContainer.GetContentPrice, IWMPContentContainer::GetContentPrice, IWMPContentContainerGetContentPrice, contentpartner/IWMPContentContainer::GetContentPrice, wmp.iwmpcontentcontainer_getcontentprice
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
 - IWMPContentContainer::GetContentPrice
 - contentpartner/IWMPContentContainer::GetContentPrice
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
 - IWMPContentContainer.GetContentPrice
---

# IWMPContentContainer::GetContentPrice


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetContentPrice</b> method retrieves the price of the media item at the specified index in the content container.

## -parameters

### -param idxContent [in]

Specifies the zero-based index of the media item for which to retrieve the price.

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

The format of the string returned in <i>pbstrPrice</i> is known only to the online store. Windows Media Player displays, but does not interpret, price strings. For more information about how Windows Media Player and the content partner plug-in exchange price information, see <a href="/windows/desktop/WMP/purchasing-media-content">Purchasing Media Content</a>.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer">IWMPContentContainer Interface</a>