---
UID: NF:contentpartner.IWMPContentPartner.GetListContents
title: IWMPContentPartner::GetListContents (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The GetListContents method initiates the retrieval of a dynamic list.
helpviewer_keywords: ["GetListContents","GetListContents method [Windows Media Player]","GetListContents method [Windows Media Player]","IWMPContentPartner interface","IWMPContentPartner interface [Windows Media Player]","GetListContents method","IWMPContentPartner.GetListContents","IWMPContentPartner::GetListContents","IWMPContentPartnerGetListContents","contentpartner/IWMPContentPartner::GetListContents","wmp.iwmpcontentpartner_getlistcontents"]
old-location: wmp\iwmpcontentpartner_getlistcontents.htm
tech.root: WMP
ms.assetid: a48935ea-8275-4b68-a1ab-006a23c455ad
ms.date: 4/26/2023
ms.keywords: GetListContents, GetListContents method [Windows Media Player], GetListContents method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],GetListContents method, IWMPContentPartner.GetListContents, IWMPContentPartner::GetListContents, IWMPContentPartnerGetListContents, contentpartner/IWMPContentPartner::GetListContents, wmp.iwmpcontentpartner_getlistcontents
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
 - IWMPContentPartner::GetListContents
 - contentpartner/IWMPContentPartner::GetListContents
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
 - IWMPContentPartner.GetListContents
---

# IWMPContentPartner::GetListContents


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetListContents</b> method initiates the retrieval of a dynamic list.

## -parameters

### -param location [in]

A library location constant that specifies the type of library view that will have its list retrieved. For example, the constant g_szCPListID specifies that a particular list will be retrieved.

### -param pContext [in]

The ID of the specific item that will have its list retrieved. For example, if <i>location</i> is g_szCPListID, then this parameter is the ID of the list that will be retrieved.

### -param bstrListType [in]

A library location constant that specifies the type of an individual list item. For example, the constant g_szCPAlbumID specifies that the items in the list are albums.

### -param bstrParams [in]

Parameters, meaningful only to the online store, associated with the retrieved list. See Remarks.

### -param dwListCookie [in]

A cookie used to identify the list retrieval operation. (The plug-in passes this cookie to <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents">IWMPContentPartnerCallback::AddListContents</a> and <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-listcontentscomplete">IWMPContentPartnerCallback::ListContentsComplete</a>.)

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

Retrieving list contents is an asynchronous operation. This method should initiate the retrieval and return immediately. Then the plug-in must make one or more calls to <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents">IWMPContentPartnerCallback::AddListContents</a> to supply Windows Media Player with the requested list contents. When the plug-in has supplied all the data, it must call <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-listcontentscomplete">IWMPContentPartnerCallback::ListContentsComplete</a> to signal the end of the operation. In each case, the plug-in passes the cookie provided in <i>dwListCookie</i> to identify the correct list retrieval session.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>