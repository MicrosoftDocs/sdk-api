---
UID: NF:dwrite_3.IDWriteFontFaceReference.GetLocalFileSize
title: IDWriteFontFaceReference::GetLocalFileSize (dwrite_3.h)
description: Get the local size of the font face in bytes, which will always be less than or equal to GetFullSize. If the locality is remote, this value is zero. If full, this value will equal GetFileSize.helpviewer_keywords: ["GetLocalFileSize","GetLocalFileSize method [Direct Write]","GetLocalFileSize method [Direct Write]","IDWriteFontFaceReference interface","IDWriteFontFaceReference interface [Direct Write]","GetLocalFileSize method","IDWriteFontFaceReference.GetLocalFileSize","IDWriteFontFaceReference::GetLocalFileSize","directwrite.idwritefontfacereference_getlocalfilesize","dwrite_3/IDWriteFontFaceReference::GetLocalFileSize"]
old-location: directwrite\idwritefontfacereference_getlocalfilesize.htm
tech.root: DirectWrite
ms.assetid: f6dc5cf5-131f-a451-7979-3ae8613577bb
ms.date: 12/05/2018
ms.keywords: GetLocalFileSize, GetLocalFileSize method [Direct Write], GetLocalFileSize method [Direct Write],IDWriteFontFaceReference interface, IDWriteFontFaceReference interface [Direct Write],GetLocalFileSize method, IDWriteFontFaceReference.GetLocalFileSize, IDWriteFontFaceReference::GetLocalFileSize, directwrite.idwritefontfacereference_getlocalfilesize, dwrite_3/IDWriteFontFaceReference::GetLocalFileSize
f1_keywords:
- dwrite_3/IDWriteFontFaceReference.GetLocalFileSize
dev_langs:
- c++
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteFontFaceReference.GetLocalFileSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontFaceReference::GetLocalFileSize


## -description


Get the local size of the font face in bytes, which will always be   
   less than or equal to GetFullSize. If the locality is remote, this     
   value is zero. If full, this value will equal GetFileSize.


## -parameters






## -returns



Type: <b>UINT64</b>

the local size of the font face in bytes, which will always be   
     less than or equal to GetFullSize. If the locality is remote, this     
     value is zero. If full, this value will equal <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-getfilesize">GetFileSize</a>.




## -see-also




<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a>
 

 

