---
UID: NF:ocidl.IPicture.SelectPicture
title: IPicture::SelectPicture (ocidl.h)
description: Selects a bitmap picture into a given device context, and returns the device context in which the picture was previously selected as well as the picture's GDI handle. This method works in conjunction with IPicture::get_CurDC.
helpviewer_keywords: ["IPicture interface [COM]","SelectPicture method","IPicture.SelectPicture","IPicture::SelectPicture","SelectPicture","SelectPicture method [COM]","SelectPicture method [COM]","IPicture interface","_ctrl_ipicture_selectpicture","com.ipicture_selectpicture","ocidl/IPicture::SelectPicture"]
old-location: com\ipicture_selectpicture.htm
tech.root: com
ms.assetid: 4168dbf7-ccc3-49ee-9b04-b0370eb389af
ms.date: 12/05/2018
ms.keywords: IPicture interface [COM],SelectPicture method, IPicture.SelectPicture, IPicture::SelectPicture, SelectPicture, SelectPicture method [COM], SelectPicture method [COM],IPicture interface, _ctrl_ipicture_selectpicture, com.ipicture_selectpicture, ocidl/IPicture::SelectPicture
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
 - IPicture::SelectPicture
 - ocidl/IPicture::SelectPicture
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
 - IPicture.SelectPicture
---

# IPicture::SelectPicture


## -description

Selects a bitmap picture into a given device context, and returns the device context in which the picture was previously selected as well as the picture's GDI handle. This method works in conjunction with <a href="/windows/desktop/api/ocidl/nf-ocidl-ipicture-get_curdc">IPicture::get_CurDC</a>.

## -parameters

### -param hDCIn [in]

A handle for the device context in which to select the picture.

### -param phDCOut [out]

A pointer to a variable that receives the previous device context. This parameter can be <b>NULL</b> if the caller does not need this information. Ownership of the device context is always the responsibility of the caller.

### -param phBmpOut [out]

A pointer to a variable that receives the GDI handle of the picture. This parameter can be <b>NULL</b> if the caller does not need the handle. Ownership of this handle is determined by the <i>fOwn</i> parameter passed to <a href="/windows/desktop/api/olectl/nf-olectl-olecreatepictureindirect">OleCreatePictureIndirect</a>. Pictures loaded from a stream always own their resources.

## -returns

This method supports the standard return values E_FAIL, E_INVALIDARG, E_OUTOFMEMORY, and S_OK.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipicture">IPicture</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ipicture-get_curdc">IPicture::get_CurDC</a>