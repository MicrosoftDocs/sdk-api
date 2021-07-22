---
UID: NF:mfapi.MFTGetInfo
title: MFTGetInfo function (mfapi.h)
description: Gets information from the registry about a Media Foundation transform (MFT).
helpviewer_keywords: ["MFTGetInfo","MFTGetInfo function [Media Foundation]","d1bac1c7-3f9b-46b7-bdf7-c32983c648ee","mf.mftgetinfo","mfapi/MFTGetInfo"]
old-location: mf\mftgetinfo.htm
tech.root: mf
ms.assetid: d1bac1c7-3f9b-46b7-bdf7-c32983c648ee
ms.date: 12/05/2018
ms.keywords: MFTGetInfo, MFTGetInfo function [Media Foundation], d1bac1c7-3f9b-46b7-bdf7-c32983c648ee, mf.mftgetinfo, mfapi/MFTGetInfo
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
 - MFTGetInfo
 - mfapi/MFTGetInfo
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
 - MFTGetInfo
---

# MFTGetInfo function


## -description

Gets information from the registry about a Media Foundation transform (MFT).

## -parameters

### -param clsidMFT [in]

The CLSID of the MFT.

### -param pszName [out]

Receives a pointer to a wide-character string containing the friendly name of the MFT. The caller must free the string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. This parameter can be <b>NULL</b>.

### -param ppInputTypes [out]

Receives a pointer to an array of <a href="/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info">MFT_REGISTER_TYPE_INFO</a> structures. Each member of the array describes an input format that the MFT supports. The caller must free the array by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. This parameter can be <b>NULL</b>.

### -param pcInputTypes [out]

Receives the number of elements in the <i>ppInputTypes</i> array. If <i>ppInputTypes</i> is <b>NULL</b>, this parameter is ignored and can be <b>NULL</b>.

### -param ppOutputTypes [out]

Receives a pointer to an array of <a href="/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info">MFT_REGISTER_TYPE_INFO</a> structures. Each member of the array describes an output format that the MFT supports. The caller must free the array by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. This parameter can be <b>NULL</b>.

### -param pcOutputTypes [out]

Receives the number of elements in the <i>ppOutputType</i> array. If <i>ppOutputTypes</i> is <b>NULL</b>, this parameter is ignored and can be <b>NULL</b>.

### -param ppAttributes [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of an attribute store. The caller must release the interface. The attribute store might contain attributes that are stored in the registry for the specified MFT. (For more information, see <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a>.)  If no attributes are stored in the registry for this MFT, the attribute store is empty. 

This parameter can be <b>NULL</b>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mftenum">MFTEnum</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>



<a href="/windows/desktop/medfound/registering-and-enumerating-mfts">Registering and Enumerating MFTs</a>