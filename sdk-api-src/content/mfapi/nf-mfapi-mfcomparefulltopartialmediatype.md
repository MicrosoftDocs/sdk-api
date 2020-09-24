---
UID: NF:mfapi.MFCompareFullToPartialMediaType
title: MFCompareFullToPartialMediaType function (mfapi.h)
description: Compares a full media type to a partial media type.
helpviewer_keywords: ["5659cc69-46dc-4b08-96c4-e9ec787a310a","MFCompareFullToPartialMediaType","MFCompareFullToPartialMediaType function [Media Foundation]","mf.mfcomparefulltopartialmediatype","mfapi/MFCompareFullToPartialMediaType"]
old-location: mf\mfcomparefulltopartialmediatype.htm
tech.root: mf
ms.assetid: 5659cc69-46dc-4b08-96c4-e9ec787a310a
ms.date: 12/05/2018
ms.keywords: 5659cc69-46dc-4b08-96c4-e9ec787a310a, MFCompareFullToPartialMediaType, MFCompareFullToPartialMediaType function [Media Foundation], mf.mfcomparefulltopartialmediatype, mfapi/MFCompareFullToPartialMediaType
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCompareFullToPartialMediaType
 - mfapi/MFCompareFullToPartialMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCompareFullToPartialMediaType
---

# MFCompareFullToPartialMediaType function


## -description

Compares a full media type to a partial media type.

## -parameters

### -param pMFTypeFull

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the full media type.

### -param pMFTypePartial

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the partial media type.

## -returns

If the full media type is compatible with the partial media type, the function returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.

## -remarks

A pipeline component can return a partial media type to describe a range of possible formats the component might accept. A partial media type has at least a major type GUID, but might be missing some of the other attributes that are needed to fully describe the type. The missing attributes represent "don't care" values for the partial type. For example, a partial video type might be missing the attributes for the width and height of the video.

This function returns <b>TRUE</b> if the following conditions are both true:

<ul>
<li>The partial media type contains a major type GUID.
          </li>
<li>All of the attributes in the partial type exist in the full type and are set to the same value.
          </li>
</ul>
Otherwise, the function returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>