---
UID: NF:mfmediaengine.IMFTimedTextBinary.GetData
title: IMFTimedTextBinary::GetData (mfmediaengine.h)
description: Gets the data content of the timed-text object.
helpviewer_keywords: ["GetData","GetData method [Media Foundation]","GetData method [Media Foundation]","IMFTimedTextBinary interface","IMFTimedTextBinary interface [Media Foundation]","GetData method","IMFTimedTextBinary.GetData","IMFTimedTextBinary::GetData","mf.imftimedtextbinary_getdata","mfmediaengine/IMFTimedTextBinary::GetData"]
old-location: mf\imftimedtextbinary_getdata.htm
tech.root: mf
ms.assetid: F8A0770D-87DD-4253-81F6-A002BEB8B896
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [Media Foundation], GetData method [Media Foundation],IMFTimedTextBinary interface, IMFTimedTextBinary interface [Media Foundation],GetData method, IMFTimedTextBinary.GetData, IMFTimedTextBinary::GetData, mf.imftimedtextbinary_getdata, mfmediaengine/IMFTimedTextBinary::GetData
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - IMFTimedTextBinary::GetData
 - mfmediaengine/IMFTimedTextBinary::GetData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFTimedTextBinary.GetData
---

# IMFTimedTextBinary::GetData


## -description

Gets the data content of the timed-text object.

## -parameters

### -param data [out]

Type: <b>const BYTE**</b>

A pointer to a memory block that receives a pointer to the data content of the timed-text object.

### -param length [out]

Type: <b>DWORD*</b>

A pointer to a variable that receives the length in bytes of the data content.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextbinary">IMFTimedTextBinary</a>