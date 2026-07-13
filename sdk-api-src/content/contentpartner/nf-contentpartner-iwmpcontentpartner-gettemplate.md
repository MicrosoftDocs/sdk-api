---
UID: NF:contentpartner.IWMPContentPartner.GetTemplate
title: IWMPContentPartner::GetTemplate (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["GetTemplate","GetTemplate method [Windows Media Player]","GetTemplate method [Windows Media Player]","IWMPContentPartner interface","IWMPContentPartner interface [Windows Media Player]","GetTemplate method","IWMPContentPartner.GetTemplate","IWMPContentPartner::GetTemplate","IWMPContentPartnerGetTemplate","contentpartner/IWMPContentPartner::GetTemplate","wmp.iwmpcontentpartner_gettemplate"]
old-location: wmp\iwmpcontentpartner_gettemplate.htm
tech.root: WMP
ms.assetid: 4bfe7d84-9f65-4bd4-867a-65c96291397d
ms.date: 4/26/2023
ms.keywords: GetTemplate, GetTemplate method [Windows Media Player], GetTemplate method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],GetTemplate method, IWMPContentPartner.GetTemplate, IWMPContentPartner::GetTemplate, IWMPContentPartnerGetTemplate, contentpartner/IWMPContentPartner::GetTemplate, wmp.iwmpcontentpartner_gettemplate
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
 - IWMPContentPartner::GetTemplate
 - contentpartner/IWMPContentPartner::GetTemplate
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
 - IWMPContentPartner.GetTemplate
---

# IWMPContentPartner::GetTemplate


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetTemplate</b> method retrieves the URL of the discovery page to be displayed when the library view changes in Windows Media Player.

## -parameters

### -param task [in]

A member of the <a href="/windows/desktop/api/contentpartner/ne-contentpartner-wmptasktype">WMPTaskType</a> enumeration that specifies the active task pane.

### -param location [in]

A <a href="/windows/desktop/WMP/library-location-constants">library location constant</a> that specifies the type of library view the user is currently seeing. For example, the constant g_szCPListID specifies that the user is viewing a pane that shows a particular playlist.

### -param pContext [in]

The ID of the specific item the user is currently seeing. For example, if <i>location</i> is g_szCPListID, then this parameter specifies the ID of the particular playlist that the user is seeing.

### -param clickLocation [in]

A library location constant that specifies the type of item the user has selected. For example, the constant g_szCPTrackID specifies that the user has selected a particular music track.

### -param pClickContext [in]

The ID of the particular item the user has selected. For example, if <i>clickLocation</i> is g_szCPTrackID, then this parameter specifies the ID of the particular track that the user has selected.

### -param bstrFilter [in]

The filter for the current library view. This is the text that the user entered in the Player's word wheel control.

### -param bstrViewParams [in]

Parameters, meaningful only to the online store, associated with the new library location. See Remarks.

### -param pbstrTemplateURL [out]

Pointer to a <b>BSTR</b> that receives the URL of the discovery page to display.

### -param pTemplateSize [out]

Receives a member of the <a href="/windows/desktop/api/contentpartner/ne-contentpartner-wmptemplatesize">WMPTemplateSize</a> enumeration that indicates the size of the template in which the Player will display the discovery page.

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

Windows Media Player calls this method when the view changes in the <b>Library</b>, <b>Sync</b>, or <b>Burn</b> pane. The Player also calls this method when one of those three panes becomes active. The pane or view can change as a result of user navigation or as the result of a call from the discovery page.

When the discovery page calls <a href="/windows/desktop/WMP/external-changeview">External.changeView</a>, it sets the <i>ViewParams</i> parameter to whatever context it wants to associate with the new view. Windows Media Player passes that context along to the plug-in in the <i>bstrViewParams</i> parameter of <b>GetTemplate</b>.

When the discovery page calls <a href="/windows/desktop/WMP/external-changeviewonlinelist">External.changeViewOnlineList</a>, it sets the <i>Params</i> parameter to whatever context it wants to associate with the new view. Windows Media Player passes that context along to the plug-in in the <i>bstrViewParams</i> parameter of <b>GetTemplate</b>.

If the view changes as a result of user navigation, Windows Media Player sets the <i>bstrParams</i> parameter to <b>NULL</b> when it calls <b>GetTemplate</b>.

Windows Media Player calls <b>GetTemplate</b> to retrieve the URL of the discovery page that it should display in the new view. The Player also receives a <b>WMPTemplateSize</b> value that indicates what portion of the new view should be occupied by the discovery page.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>