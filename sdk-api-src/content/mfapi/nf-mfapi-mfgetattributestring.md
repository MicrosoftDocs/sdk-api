---
UID: NF:mfapi.MFGetAttributeString
title: MFGetAttributeString function (mfapi.h)
description: Gets a string value from an attribute store.
helpviewer_keywords: ["MFGetAttributeString","MFGetAttributeString function [Media Foundation]","mf.mfgetattributestring","mfapi/MFGetAttributeString"]
old-location: mf\mfgetattributestring.htm
tech.root: mf
ms.assetid: 6CA416AB-5EA1-4A85-A421-1CDD3D111296
ms.date: 12/05/2018
ms.keywords: MFGetAttributeString, MFGetAttributeString function [Media Foundation], mf.mfgetattributestring, mfapi/MFGetAttributeString
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - MFGetAttributeString
 - mfapi/MFGetAttributeString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFGetAttributeString
---

# MFGetAttributeString function


## -description

Gets a string value from an attribute store.

## -parameters

### -param pAttributes [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface.

### -param guidKey [in]

A GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_STRING</b>.

### -param ppsz [out]

If the key is found and the value is a string type, this parameter receives a copy of the string. The caller must free the memory for the string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is a wrapper for the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring">IMFAttributes::GetAllocatedString</a> method.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>