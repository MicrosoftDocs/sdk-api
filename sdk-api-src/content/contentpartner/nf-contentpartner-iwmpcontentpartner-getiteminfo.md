---
UID: NF:contentpartner.IWMPContentPartner.GetItemInfo
title: IWMPContentPartner::GetItemInfo (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["GetItemInfo","GetItemInfo method [Windows Media Player]","GetItemInfo method [Windows Media Player]","IWMPContentPartner interface","IWMPContentPartner interface [Windows Media Player]","GetItemInfo method","IWMPContentPartner.GetItemInfo","IWMPContentPartner::GetItemInfo","IWMPContentPartnerGetItemInfo","contentpartner/IWMPContentPartner::GetItemInfo","wmp.iwmpcontentpartner_getiteminfo"]
old-location: wmp\iwmpcontentpartner_getiteminfo.htm
tech.root: WMP
ms.assetid: b7355c45-fb58-45f4-b7e4-3dd2c3f8c918
ms.date: 4/26/2023
ms.keywords: GetItemInfo, GetItemInfo method [Windows Media Player], GetItemInfo method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],GetItemInfo method, IWMPContentPartner.GetItemInfo, IWMPContentPartner::GetItemInfo, IWMPContentPartnerGetItemInfo, contentpartner/IWMPContentPartner::GetItemInfo, wmp.iwmpcontentpartner_getiteminfo
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
 - IWMPContentPartner::GetItemInfo
 - contentpartner/IWMPContentPartner::GetItemInfo
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
 - IWMPContentPartner.GetItemInfo
---

# IWMPContentPartner::GetItemInfo


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetItemInfo</b> method retrieves information (for example, a URL or a caption) related to an item owned by an online store.

## -parameters

### -param bstrInfoName [in]

<b>BSTR</b> specifying the item for which information will be retrieved. See Remarks for possible values.

### -param pContext [in]

Pointer to a <b>VARIANT</b> that supplies contextual information for the requested information.

### -param pData [out]

Pointer to a <b>VARIANT</b> that receives the information.

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

The following list gives possible values for the <i>bstrInfoName</i> parameter and corresponding values for the <i>pContext</i> and <i>pData</i> parameters.

g_szItemInfo_AlbumArtURL

The <i>pContext</i> parameter supplies a <b>VT_UI4</b> that is the ID of an album in the online store's catalog.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of the art that Windows Media Player will display for the album.

g_szItemInfo_ALTLoginURL

The <i>pContext</i> parameter has type <b>VT_EMPTY</b> and supplies no information.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of a webpage that Windows Media Player will display as an alternative to the standard log-in dialog box. Windows Media Player requests the alternative log-in URL only if the <b>SUBSCRIPTION_CAP_ALTLOGIN</b> flag is set in the <b>Capabilities</b> registry entry for the online store's plug-in. For more information about the <b>Capabilities</b> registry entry, see <a href="/windows/desktop/WMP/registry-keys-and-entries-for-a-type-1-online-store">Registry Keys and Entries for a Type 1 Online Store</a>.

The online store can specify the size of the window that hosts the alternative log-in page by appending the parameter string ?DlgX=<i>width</i>&amp;DlgY=<i>height</i> to the URL. In the parameter string, <i>width</i> and <i>height</i> are the width and height of the window in pixels. For example <b>GetItemInfo</b> could return the following string to specify that AltLogin.htm should be displayed in a window that has a width of 800 pixels and a height of 400 pixels:

http://proseware.com/AltLogin.htm?DlgX=800&amp;DlgY=400

g_szItemInfo_ALTLoginCaption

The <i>pContext</i> parameter has type <b>VT_EMPTY</b> and supplies no information.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the caption for the window that Windows Media Player will open to host the alternative log-in webpage.

g_szItemInfo_ArtistArtURL

The <i>pContext</i> parameter supplies a <b>VT_UI4</b> that is the ID of an artist in the online store's catalog.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of the art that Windows Media Player will display for the artist.

g_szItemInfo_AuthenticationSuccessURL

The <i>pContext</i> parameter supplies a <b>VT_I4</b> that is the index of a webpage, provided by the online store, that Windows Media Player will display after successful authentication.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of the webpage. Note that indexes for webpages that represent authentication success are not interpreted by Windows Media Player; they have meaning only to the online store.

g_szItemInfo_ErrorDescription

The <i>pContext</i> parameter supplies a <b>VT_ERROR</b> that is an <b>HRESULT</b> that the plug-in previously supplied to the Player. For example, the plug-in supplies an <b>HRESULT</b> when it calls <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete">IWMPContentPartnerCallback::BuyComplete</a>.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the error description created by the online store and associated with the <b>HRESULT</b>. Windows Media Player displays the error message but does not interpret it.

g_szItemInfo_ErrorURL

The <i>pContext</i> parameter supplies a <b>VT_ERROR</b> that is an <b>HRESULT</b> that the plug-in previously supplied to the Player. For example, the plug-in supplies an <b>HRESULT</b> when it calls <b>IWMPContentPartnerCallback::BuyComplete</b>.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of the webpage that Windows Media Player will display when the user clicks the error-resolving link. The error-resolving link is part of the user interface of the Player.

g_szItemInfo_ErrorURLLinkText

The <i>pContext</i> parameter supplies a <b>VT_ERROR</b> that is an <b>HRESULT</b> that the plug-in previously supplied to the Player. For example, the plug-in supplies an <b>HRESULT</b> when it calls <b>IWMPContentPartnerCallback::BuyComplete</b>.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the text, created by the online store, that Windows Media Player will use when it displays the error-resolving link.

g_szItemInfo_TreeListIconURL

The <i>pContext</i> parameter supplies a <b>VT_UI4</b> that is the ID of a list in the online store's catalog.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of the icon that Windows Media Player will display, in the tree-view control, for the list.

g_szItemInfo_CreateAccountURL

The <i>pContext</i> parameter has type <b>VT_EMPTY</b> and supplies no information.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of the webpage that Windows Media Player will display to enable the user to manage his or her account.

g_szItemInfo_ForgetPasswordURL

The <i>pContext</i> parameter has type <b>VT_EMPTY</b> and supplies no information.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of the webpage that Windows Media Player will display when the user forgets his or her password.

g_szItemInfo_GenreArtURL

The <i>pContext</i> parameter supplies a <b>VT_UI4</b> that is the ID of a genre in the online store's catalog.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of the art that Windows Media Player will display for the genre.

g_szItemInfo_HTMLViewURL

The <i>pContext</i> parameter supplies a <b>VT_BSTR</b> that is a string that Windows Media Player obtained from a <a href="/windows/desktop/WMP/param-element">PARAM</a> element in a Windows Media metafile (ASX file).

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of the webpage that Windows Media Player will display.

When the <b>name</b> attribute of a <b>PARAM</b> element is "HTMLFlink", Windows Media Player passes the <b>value</b> attribute of the PARAM element to this method to retrieve the URL of a Web Page to display in the <b>Now Playing</b> feature.

g_szItemInfo_ListArtURL

The <i>pContext</i> parameter supplies a <b>VT_UI4</b> that is the ID of a list in the online store's catalog.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of the art that Windows Media Player will display for the list.

g_szItemInfo_LoginFailureURL

The <i>pContext</i> parameter supplies a <b>VT_UI4</b> that is the index of a webpage, provided by the online store, that Windows Media Player will display after a log-in failure.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of the webpage.

Windows Media Player previously obtained the index when the online store's plug-in called <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify">IWMPContentPartnerCallback::Notify</a>, passing wmpcnLoginStateChange in the <i>type</i> parameter. The indexes of log-in failure webpages are not interpreted by Windows Media Player; they have meaning only to the online store.

g_szItemInfo_PopupURL

The <i>pContext</i> parameter supplies a <b>VT_I4</b> that is the index of a pop-up webpage, provided by the online store, that Windows Media Player will display in a modal window.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of the webpage to display in the modal window. Indexes of pop-up webpages are not interpreted by Windows Media Player; they have meaning only to the online store.

g_szItemInfo_PopupCaption

The <i>pContext</i> parameter supplies a <b>VT_I4</b> that is the index of a pop-up caption created by the online store.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the caption for the window that Windows Media Player will open to host the pop-up webpage. Pop-up caption indexes are not interpreted by Windows Media Player; they have meaning only to the online store.

g_szItemInfo_RadioArtURL

The <i>pContext</i> parameter supplies a <b>VT_UI4</b> that is the ID of a radio feed in the online store's catalog.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of the art that Windows Media Player will display for the radio feed.

g_szItemInfo_SubGenreArtURL

The <i>pContext</i> parameter supplies a <b>VT_UI4</b> that is the ID of a subgenre in the online store's catalog.

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that is the URL of the art that Windows Media Player will display for the subgenre.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>