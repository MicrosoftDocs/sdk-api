---
UID: NF:amvideo.IFullScreenVideoEx.CountModes
title: IFullScreenVideoEx::CountModes (amvideo.h)
description: The CountModes method retrieves the number of display modes that the Full Screen Renderer supports.
helpviewer_keywords: ["CountModes","CountModes method [DirectShow]","CountModes method [DirectShow]","IFullScreenVideoEx interface","IFullScreenVideoCountModes","IFullScreenVideoEx interface [DirectShow]","CountModes method","IFullScreenVideoEx.CountModes","IFullScreenVideoEx::CountModes","amvideo/IFullScreenVideoEx::CountModes","dshow.ifullscreenvideoex_countmodes"]
old-location: dshow\ifullscreenvideoex_countmodes.htm
tech.root: dshow
ms.assetid: 70d4e124-083b-4729-8f39-778e815ea23b
ms.date: 12/05/2018
ms.keywords: CountModes, CountModes method [DirectShow], CountModes method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoCountModes, IFullScreenVideoEx interface [DirectShow],CountModes method, IFullScreenVideoEx.CountModes, IFullScreenVideoEx::CountModes, amvideo/IFullScreenVideoEx::CountModes, dshow.ifullscreenvideoex_countmodes
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFullScreenVideoEx::CountModes
 - amvideo/IFullScreenVideoEx::CountModes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFullScreenVideoEx.CountModes
---

# IFullScreenVideoEx::CountModes


## -description

The <code>CountModes</code> method retrieves the number of display modes that the Full Screen Renderer supports.

## -parameters

### -param pModes [out]

Pointer to the returned mode count.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>