---
UID: NF:shobjidl_core.IExtractImage.Extract
title: IExtractImage::Extract (shobjidl_core.h)
description: Requests an image from an object, such as an item in a Shell folder.
helpviewer_keywords: ["Extract","Extract method [Windows Shell]","Extract method [Windows Shell]","IExtractImage interface","IExtractImage interface [Windows Shell]","Extract method","IExtractImage.Extract","IExtractImage::Extract","_win32_IExtractImage_Extract","shell.IExtractImage_Extract","shobjidl_core/IExtractImage::Extract"]
old-location: shell\IExtractImage_Extract.htm
tech.root: shell
ms.assetid: 7c40e2cf-c706-4a4a-819f-a416d6846158
ms.date: 12/05/2018
ms.keywords: Extract, Extract method [Windows Shell], Extract method [Windows Shell],IExtractImage interface, IExtractImage interface [Windows Shell],Extract method, IExtractImage.Extract, IExtractImage::Extract, _win32_IExtractImage_Extract, shell.IExtractImage_Extract, shobjidl_core/IExtractImage::Extract
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 4.70 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExtractImage::Extract
 - shobjidl_core/IExtractImage::Extract
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IExtractImage.Extract
---

# IExtractImage::Extract


## -description

Requests an image from an object, such as an item in a Shell folder.

## -parameters

### -param phBmpThumbnail [out]

Type: <b>HBITMAP*</b>

The buffer to hold the bitmapped image.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.

## -remarks

You must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage-getlocation">IExtractImage::GetLocation</a> prior to calling <b>Extract</b>.