---
UID: NF:coml2api.ReadClassStm
title: ReadClassStm function (coml2api.h)
description: Reads the CLSID previously written to a stream object with the WriteClassStm function.
helpviewer_keywords: ["ReadClassStm","ReadClassStm function [Structured Storage]","_stg_readclassstm","coml2api/ReadClassStm","stg.readclassstm"]
old-location: stg\readclassstm.htm
tech.root: Stg
ms.assetid: bcf11c5b-e164-4a0f-b30f-ee9e76c4356d
ms.date: 12/05/2018
ms.keywords: ReadClassStm, ReadClassStm function [Structured Storage], _stg_readclassstm, coml2api/ReadClassStm, stg.readclassstm
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
 - ReadClassStm
 - coml2api/ReadClassStm
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
 - ReadClassStm
---

# ReadClassStm function


## -description

The 
<b>ReadClassStm</b> function
			reads the CLSID previously written to a stream object with the 
<a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstm">WriteClassStm</a> function.

## -parameters

### -param pStm [in]

A pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface on the stream object that contains the CLSID to be read. This CLSID must have been previously written to the stream object using 
<a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstm">WriteClassStm</a>.

### -param pclsid [out]

A pointer to where the CLSID is to be written.

## -returns

This function also returns any of the error values returned by the 
<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> method.

## -remarks

Most applications do not call the 
<b>ReadClassStm</b> function directly. COM calls it before making a call to an object's 
<a href="/windows/desktop/api/objidl/nf-objidl-ipersiststream-load">IPersistStream::Load</a> implementation.

## -see-also

<a href="/windows/desktop/api/coml2api/nf-coml2api-readclassstg">ReadClassStg</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstg">WriteClassStg</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstm">WriteClassStm</a>