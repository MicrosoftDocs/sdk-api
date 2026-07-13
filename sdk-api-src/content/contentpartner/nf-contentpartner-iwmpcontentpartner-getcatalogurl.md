---
UID: NF:contentpartner.IWMPContentPartner.GetCatalogURL
title: IWMPContentPartner::GetCatalogURL (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["GetCatalogURL","GetCatalogURL method [Windows Media Player]","GetCatalogURL method [Windows Media Player]","IWMPContentPartner interface","IWMPContentPartner interface [Windows Media Player]","GetCatalogURL method","IWMPContentPartner.GetCatalogURL","IWMPContentPartner::GetCatalogURL","IWMPContentPartnerGetCatalogURL","contentpartner/IWMPContentPartner::GetCatalogURL","wmp.iwmpcontentpartner_getcatalogurl"]
old-location: wmp\iwmpcontentpartner_getcatalogurl.htm
tech.root: WMP
ms.assetid: 291440d5-b6d3-4586-98d2-3f7c56da29aa
ms.date: 4/26/2023
ms.keywords: GetCatalogURL, GetCatalogURL method [Windows Media Player], GetCatalogURL method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],GetCatalogURL method, IWMPContentPartner.GetCatalogURL, IWMPContentPartner::GetCatalogURL, IWMPContentPartnerGetCatalogURL, contentpartner/IWMPContentPartner::GetCatalogURL, wmp.iwmpcontentpartner_getcatalogurl
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
 - IWMPContentPartner::GetCatalogURL
 - contentpartner/IWMPContentPartner::GetCatalogURL
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
 - IWMPContentPartner.GetCatalogURL
---

# IWMPContentPartner::GetCatalogURL


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetCatalogURL</b> method retrieves the URL from which to retrieve an update to the online store's current catalog.

## -parameters

### -param dwCatalogVersion [in]

<b>DWORD</b> containing the current catalog version.

### -param dwCatalogSchemaVersion [in]

<b>DWORD</b> containing the current catalog schema version.

### -param catalogLCID [in]

The locale ID (LCID) for the catalog.

### -param pdwNewCatalogVersion [out]

Address of a <b>DWORD</b> that receives the new catalog version.

### -param pbstrCatalogURL [out]

Address of a <b>BSTR</b> that receives the URL.

### -param pExpirationDate [out]

Address of a <b>VARIANT</b> (<b>VT_DATE</b>) that receives the expiration date of the catalog update.

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

We recommend that the catalog URL specify the version as part of the path. For example, `http://www.contoso.com/Catalogs/210/catalog.wmdb`.

## -see-also

<a href="/windows/desktop/WMP/catalog-compiler-for-type-1-online-stores">Catalog Compiler for Type 1 Online Stores</a>



<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>



<a href="/windows/desktop/WMP/music-catalog">Music Catalog</a>
