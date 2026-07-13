---
UID: NF:coml2api.WriteClassStg
title: WriteClassStg function (coml2api.h)
description: The WriteClassStg function stores the specified class identifier (CLSID) in a storage object.
helpviewer_keywords: ["WriteClassStg","WriteClassStg function [Structured Storage]","_stg_writeclassstg","coml2api/WriteClassStg","stg.writeclassstg"]
old-location: stg\writeclassstg.htm
tech.root: Stg
ms.assetid: 5f2f16d1-923f-4ba7-8d4b-7e8535f6f15e
ms.date: 12/05/2018
ms.keywords: WriteClassStg, WriteClassStg function [Structured Storage], _stg_writeclassstg, coml2api/WriteClassStg, stg.writeclassstg
req.header: coml2api.h
req.include-header: Ole2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WriteClassStg
 - coml2api/WriteClassStg
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - WriteClassStg
---

# WriteClassStg function


## -description

The <b>WriteClassStg</b> function stores the specified class identifier (CLSID) in a storage object.

## -parameters

### -param pStg [in]

<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer to the storage object that gets a new CLSID.

### -param rclsid [in]

Pointer to the CLSID to be stored with the object.

## -returns

This function returns HRESULT.

## -remarks

The 
<b>WriteClassStg</b> function writes a CLSID to the specified storage object so that it can be read by the 
<a href="/windows/desktop/api/coml2api/nf-coml2api-readclassstg">ReadClassStg</a> function. Container applications typically call this function before calling the 
<a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-save">IPersistStorage::Save</a> method.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-olesave">OleSave</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-readclassstg">ReadClassStg</a>