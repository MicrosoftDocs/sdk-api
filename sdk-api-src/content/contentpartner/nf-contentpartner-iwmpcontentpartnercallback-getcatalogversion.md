---
UID: NF:contentpartner.IWMPContentPartnerCallback.GetCatalogVersion
title: IWMPContentPartnerCallback::GetCatalogVersion (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["GetCatalogVersion","GetCatalogVersion method [Windows Media Player]","GetCatalogVersion method [Windows Media Player]","IWMPContentPartnerCallback interface","IWMPContentPartnerCallback interface [Windows Media Player]","GetCatalogVersion method","IWMPContentPartnerCallback.GetCatalogVersion","IWMPContentPartnerCallback::GetCatalogVersion","IWMPContentPartnerCallbackGetCatalogVersion","contentpartner/IWMPContentPartnerCallback::GetCatalogVersion","wmp.iwmpcontentpartnercallback_getcatalogversion"]
old-location: wmp\iwmpcontentpartnercallback_getcatalogversion.htm
tech.root: WMP
ms.assetid: e77785d1-71e3-474d-bad1-4b1145a06d01
ms.date: 4/26/2023
ms.keywords: GetCatalogVersion, GetCatalogVersion method [Windows Media Player], GetCatalogVersion method [Windows Media Player],IWMPContentPartnerCallback interface, IWMPContentPartnerCallback interface [Windows Media Player],GetCatalogVersion method, IWMPContentPartnerCallback.GetCatalogVersion, IWMPContentPartnerCallback::GetCatalogVersion, IWMPContentPartnerCallbackGetCatalogVersion, contentpartner/IWMPContentPartnerCallback::GetCatalogVersion, wmp.iwmpcontentpartnercallback_getcatalogversion
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
 - IWMPContentPartnerCallback::GetCatalogVersion
 - contentpartner/IWMPContentPartnerCallback::GetCatalogVersion
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
 - IWMPContentPartnerCallback.GetCatalogVersion
---

# IWMPContentPartnerCallback::GetCatalogVersion


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetCatalogVersion</b> method retrieves the version information for the online store catalog currently in use by Windows Media Player.

## -parameters

### -param pdwVersion [out]

Address of a <b>DWORD</b> that receives the catalog version.

### -param pdwSchemaVersion [out]

Address of a <b>DWORD</b> that receives the schema version.

### -param plcid [out]

Address of an <b>LCID</b> that receives the locale ID for the catalog.

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