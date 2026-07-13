---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetName
title: IMFTimedTextStyle::GetName (mfmediaengine.h)
description: Gets the name of the timed-text style.
helpviewer_keywords: ["GetName","GetName method [Media Foundation]","GetName method [Media Foundation]","IMFTimedTextStyle interface","IMFTimedTextStyle interface [Media Foundation]","GetName method","IMFTimedTextStyle.GetName","IMFTimedTextStyle::GetName","mf.imftimedtextstyle_getname","mfmediaengine/IMFTimedTextStyle::GetName"]
old-location: mf\imftimedtextstyle_getname.htm
tech.root: mf
ms.assetid: C1B28336-27D1-4592-B583-940C2C9EF9A0
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Media Foundation], GetName method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetName method, IMFTimedTextStyle.GetName, IMFTimedTextStyle::GetName, mf.imftimedtextstyle_getname, mfmediaengine/IMFTimedTextStyle::GetName
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
 - IMFTimedTextStyle::GetName
 - mfmediaengine/IMFTimedTextStyle::GetName
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
 - IMFTimedTextStyle.GetName
---

# IMFTimedTextStyle::GetName


## -description

Gets the name of the timed-text style.

## -parameters

### -param name [out]

Type: <b>LPCWSTR*</b>

A pointer to a variable that receives the null-terminated wide-character string that contains the name of the style.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a>