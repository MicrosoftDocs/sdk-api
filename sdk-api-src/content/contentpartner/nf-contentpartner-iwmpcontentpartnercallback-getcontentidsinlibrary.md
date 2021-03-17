---
UID: NF:contentpartner.IWMPContentPartnerCallback.GetContentIDsInLibrary
title: IWMPContentPartnerCallback::GetContentIDsInLibrary (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["GetContentIDsInLibrary","GetContentIDsInLibrary method [Windows Media Player]","GetContentIDsInLibrary method [Windows Media Player]","IWMPContentPartnerCallback interface","IWMPContentPartnerCallback interface [Windows Media Player]","GetContentIDsInLibrary method","IWMPContentPartnerCallback.GetContentIDsInLibrary","IWMPContentPartnerCallback::GetContentIDsInLibrary","IWMPContentPartnerCallbackGetContentIDsInLibrary","contentpartner/IWMPContentPartnerCallback::GetContentIDsInLibrary","wmp.iwmpcontentpartnercallback_getcontentidsinlibrary"]
old-location: wmp\iwmpcontentpartnercallback_getcontentidsinlibrary.htm
tech.root: WMP
ms.assetid: c8fbac82-77dc-4316-860d-cdf53e8bb9a7
ms.date: 12/05/2018
ms.keywords: GetContentIDsInLibrary, GetContentIDsInLibrary method [Windows Media Player], GetContentIDsInLibrary method [Windows Media Player],IWMPContentPartnerCallback interface, IWMPContentPartnerCallback interface [Windows Media Player],GetContentIDsInLibrary method, IWMPContentPartnerCallback.GetContentIDsInLibrary, IWMPContentPartnerCallback::GetContentIDsInLibrary, IWMPContentPartnerCallbackGetContentIDsInLibrary, contentpartner/IWMPContentPartnerCallback::GetContentIDsInLibrary, wmp.iwmpcontentpartnercallback_getcontentidsinlibrary
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
 - IWMPContentPartnerCallback::GetContentIDsInLibrary
 - contentpartner/IWMPContentPartnerCallback::GetContentIDsInLibrary
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
 - IWMPContentPartnerCallback.GetContentIDsInLibrary
---

# IWMPContentPartnerCallback::GetContentIDsInLibrary


## -description

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetContentIDsInLibrary</b> method retrieves an array of content IDs that represent the music tracks in the library.

## -parameters

### -param pcContentIDs [out]

Receives the number of elements in the <i>pprgIDs</i> array.

### -param pprgIDs [out]

Receives a pointer to an array of content IDs.

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

This method allocates an array of <b>ULONGs</b>, fills the array with content IDs, and returns the address of the array in the output parameter <i>pprgIDs</i>. When the caller is finished with the array, it must free the array by calling <b>CoTaskMemFree</b>.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback">IWMPContentPartnerCallback Interface</a>