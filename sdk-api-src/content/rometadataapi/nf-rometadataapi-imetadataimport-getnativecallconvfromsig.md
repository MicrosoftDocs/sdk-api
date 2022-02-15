---
UID: NF:rometadataapi.IMetaDataImport.GetNativeCallConvFromSig
title: IMetaDataImport::GetNativeCallConvFromSig (rometadataapi.h)
description: Gets the native calling convention for the method that is represented by the specified signature pointer.
helpviewer_keywords: ["GetNativeCallConvFromSig","GetNativeCallConvFromSig method [Windows Runtime]","GetNativeCallConvFromSig method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetNativeCallConvFromSig method","IMetaDataImport.GetNativeCallConvFromSig","IMetaDataImport::GetNativeCallConvFromSig","rometadataapi/IMetaDataImport::GetNativeCallConvFromSig","winrt.imetadataimport_getnativecallconvfromsig"]
old-location: winrt\imetadataimport_getnativecallconvfromsig.htm
tech.root: WinRT
ms.assetid: 90e09d3d-c77e-44c3-b4d0-6b2aee995b1e
ms.date: 12/05/2018
ms.keywords: GetNativeCallConvFromSig, GetNativeCallConvFromSig method [Windows Runtime], GetNativeCallConvFromSig method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetNativeCallConvFromSig method, IMetaDataImport.GetNativeCallConvFromSig, IMetaDataImport::GetNativeCallConvFromSig, rometadataapi/IMetaDataImport::GetNativeCallConvFromSig, winrt.imetadataimport_getnativecallconvfromsig
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
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
 - IMetaDataImport::GetNativeCallConvFromSig
 - rometadataapi/IMetaDataImport::GetNativeCallConvFromSig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataImport.GetNativeCallConvFromSig
---

# IMetaDataImport::GetNativeCallConvFromSig


## -description

Gets the native calling convention for the method that is represented by the specified signature pointer.

## -parameters

### -param pvSig [in]

A pointer to the metadata signature of the method to return the calling convention for.

### -param cbSig [in]

The size in bytes of <i>const</i>.

### -param pCallConv [out]

A pointer to the native calling convention.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>