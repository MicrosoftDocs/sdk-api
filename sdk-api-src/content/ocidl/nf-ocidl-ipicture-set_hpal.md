---
UID: NF:ocidl.IPicture.set_hPal
title: IPicture::set_hPal (ocidl.h)
description: Assigns a GDI palette to the picture contained in the picture object.
helpviewer_keywords: ["IPicture interface [COM]","set_hPal method","IPicture.set_hPal","IPicture::set_hPal","_ctrl_ipicture_set_hpal","com.ipicture_set_hpal","ocidl/IPicture::set_hPal","set_hPal","set_hPal method [COM]","set_hPal method [COM]","IPicture interface"]
old-location: com\ipicture_set_hpal.htm
tech.root: com
ms.assetid: c20b9efd-cf85-4ee1-890b-35fde0226982
ms.date: 12/05/2018
ms.keywords: IPicture interface [COM],set_hPal method, IPicture.set_hPal, IPicture::set_hPal, _ctrl_ipicture_set_hpal, com.ipicture_set_hpal, ocidl/IPicture::set_hPal, set_hPal, set_hPal method [COM], set_hPal method [COM],IPicture interface
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IPicture::set_hPal
 - ocidl/IPicture::set_hPal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPicture.set_hPal
---

# IPicture::set_hPal


## -description

Assigns a GDI palette to the picture contained in the picture object.

## -parameters

### -param hPal [in]

A handle to the GDI palette assigned to the picture.

## -returns

This method supports the standard return values E_FAIL, E_INVALIDARG, E_OUTOFMEMORY, and S_OK.

## -remarks

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Ownership of the palette passed to this method depends on how the picture object was created, as specified by the <i>fOwn</i> parameter to <a href="/windows/desktop/api/olectl/nf-olectl-olecreatepictureindirect">OleCreatePictureIndirect</a>. <a href="/windows/desktop/api/olectl/nf-olectl-oleloadpicture">OleLoadPicture</a> forces <i>fOwn</i> to <b>TRUE</b>; if the object owns the picture, then it takes over ownership of this palette.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipicture">IPicture</a>