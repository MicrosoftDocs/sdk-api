---
UID: NF:contentpartner.IWMPContentPartnerCallback.AddListContents
title: IWMPContentPartnerCallback::AddListContents (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The AddListContents method adds a set of media items to a list.
helpviewer_keywords: ["AddListContents","AddListContents method [Windows Media Player]","AddListContents method [Windows Media Player]","IWMPContentPartnerCallback interface","IWMPContentPartnerCallback interface [Windows Media Player]","AddListContents method","IWMPContentPartnerCallback.AddListContents","IWMPContentPartnerCallback::AddListContents","IWMPContentPartnerCallbackAddListContents","contentpartner/IWMPContentPartnerCallback::AddListContents","wmp.iwmpcontentpartnercallback_addlistcontents"]
old-location: wmp\iwmpcontentpartnercallback_addlistcontents.htm
tech.root: WMP
ms.assetid: 22d28495-310e-4f3d-a0e3-8f6679c78c40
ms.date: 4/26/2023
ms.keywords: AddListContents, AddListContents method [Windows Media Player], AddListContents method [Windows Media Player],IWMPContentPartnerCallback interface, IWMPContentPartnerCallback interface [Windows Media Player],AddListContents method, IWMPContentPartnerCallback.AddListContents, IWMPContentPartnerCallback::AddListContents, IWMPContentPartnerCallbackAddListContents, contentpartner/IWMPContentPartnerCallback::AddListContents, wmp.iwmpcontentpartnercallback_addlistcontents
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
 - IWMPContentPartnerCallback::AddListContents
 - contentpartner/IWMPContentPartnerCallback::AddListContents
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
 - IWMPContentPartnerCallback.AddListContents
---

# IWMPContentPartnerCallback::AddListContents


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>AddListContents</b> method adds a set of media items to a list.

## -parameters

### -param dwListCookie [in]

A cookie that identifies a list retrieval session. Windows Media Player previously supplied this cookie to the content partner plug-in by calling <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a>.

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

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback">IWMPContentPartnerCallback Interface</a>