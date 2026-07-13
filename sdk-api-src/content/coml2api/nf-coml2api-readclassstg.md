---
UID: NF:coml2api.ReadClassStg
title: ReadClassStg function (coml2api.h)
description: The ReadClassStg function reads the CLSID previously written to a storage object with the WriteClassStg function.
helpviewer_keywords: ["ReadClassStg","ReadClassStg function [Structured Storage]","_stg_readclassstg","coml2api/ReadClassStg","stg.readclassstg"]
old-location: stg\readclassstg.htm
tech.root: Stg
ms.assetid: 90256fcd-54ce-48e1-aa12-d8f91cd4dfb1
ms.date: 12/05/2018
ms.keywords: ReadClassStg, ReadClassStg function [Structured Storage], _stg_readclassstg, coml2api/ReadClassStg, stg.readclassstg
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
 - ReadClassStg
 - coml2api/ReadClassStg
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
 - ReadClassStg
---

# ReadClassStg function


## -description

The <b>ReadClassStg</b> function
			reads the CLSID previously written to a storage object with the 
<a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstg">WriteClassStg</a> function.

## -parameters

### -param pStg [in]

Pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on the storage object containing the CLSID to be retrieved.

### -param pclsid [out]

Pointer to where the CLSID is written. May return CLSID_NULL.

## -returns

This function supports the standard return value E_OUTOFMEMORY, in addition to the following:

This function also returns any of the error values returned by the 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a> method.

## -remarks

<b>ReadClassStg</b> is a helper function that calls the <a href="/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a> method and retrieves the CLSID previously written to the storage object with a call to 
<a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstg">WriteClassStg</a> from the 
<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleload">OleLoad</a>



<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstg">WriteClassStg</a>