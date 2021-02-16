---
UID: NF:wmp.IWMPLibrary.get_mediaCollection
title: IWMPLibrary::get_mediaCollection (wmp.h)
description: The get_mediaCollection method retrieves a pointer to the IWMPMediaCollection interface for the current library.
helpviewer_keywords: ["IWMPLibrary interface [Windows Media Player]","get_mediaCollection method","IWMPLibrary.get_mediaCollection","IWMPLibrary::get_mediaCollection","IWMPLibraryget_mediaCollection","get_mediaCollection","get_mediaCollection method [Windows Media Player]","get_mediaCollection method [Windows Media Player]","IWMPLibrary interface","wmp.iwmplibrary_get_mediacollection","wmp/IWMPLibrary::get_mediaCollection"]
old-location: wmp\iwmplibrary_get_mediacollection.htm
tech.root: WMP
ms.assetid: 6de39a4e-fcce-401b-9bbf-7b06d1fb0370
ms.date: 12/05/2018
ms.keywords: IWMPLibrary interface [Windows Media Player],get_mediaCollection method, IWMPLibrary.get_mediaCollection, IWMPLibrary::get_mediaCollection, IWMPLibraryget_mediaCollection, get_mediaCollection, get_mediaCollection method [Windows Media Player], get_mediaCollection method [Windows Media Player],IWMPLibrary interface, wmp.iwmplibrary_get_mediacollection, wmp/IWMPLibrary::get_mediaCollection
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPLibrary::get_mediaCollection
 - wmp/IWMPLibrary::get_mediaCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPLibrary.get_mediaCollection
---

# IWMPLibrary::get_mediaCollection


## -description

The <b>get_mediaCollection</b> method retrieves a pointer to the <b>IWMPMediaCollection</b> interface for the current library.

## -parameters

### -param ppIWMPMediaCollection [out]

Address of a variable that receives a pointer to the <b>IWMPMediaCollection</b> interface for the current library.

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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmplibrary">IWMPLibrary Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>