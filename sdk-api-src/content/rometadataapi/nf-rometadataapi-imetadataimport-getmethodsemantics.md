---
UID: NF:rometadataapi.IMetaDataImport.GetMethodSemantics
title: IMetaDataImport::GetMethodSemantics (rometadataapi.h)
description: Gets flags indicating the relationship between the method referenced by the specified MethodDef token and the paired property and event referenced by the specified EventProp token.
helpviewer_keywords: ["GetMethodSemantics","GetMethodSemantics method [Windows Runtime]","GetMethodSemantics method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetMethodSemantics method","IMetaDataImport.GetMethodSemantics","IMetaDataImport::GetMethodSemantics","rometadataapi/IMetaDataImport::GetMethodSemantics","winrt.imetadataimport_getmethodsemantics"]
old-location: winrt\imetadataimport_getmethodsemantics.htm
tech.root: WinRT
ms.assetid: b4133bf8-4ae4-43ad-8d07-4f7805e9ef2c
ms.date: 12/05/2018
ms.keywords: GetMethodSemantics, GetMethodSemantics method [Windows Runtime], GetMethodSemantics method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetMethodSemantics method, IMetaDataImport.GetMethodSemantics, IMetaDataImport::GetMethodSemantics, rometadataapi/IMetaDataImport::GetMethodSemantics, winrt.imetadataimport_getmethodsemantics
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
 - IMetaDataImport::GetMethodSemantics
 - rometadataapi/IMetaDataImport::GetMethodSemantics
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
 - IMetaDataImport.GetMethodSemantics
---

# IMetaDataImport::GetMethodSemantics


## -description

Gets flags indicating the relationship between the method referenced by the specified MethodDef token and the paired property and event referenced by the specified EventProp token.

## -parameters

### -param tkMethodDef [in]

A MethodDef token representing the method to get the semantic role information for.

### -param tkEventProp [in]

A token representing the paired property and event for which to get the method's role.

### -param pdwSemanticsFlags [out]

A pointer to the associated semantics flags. This value is a bitmask from the CorMethodSemanticsAttr enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>