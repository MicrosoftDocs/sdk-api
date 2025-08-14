---
UID: NF:coml2api.WriteClassStm
title: WriteClassStm function (coml2api.h)
description: The WriteClassStm function stores the specified CLSID in the stream.
helpviewer_keywords: ["WriteClassStm","WriteClassStm function [Structured Storage]","_stg_writeclassstm","coml2api/WriteClassStm","stg.writeclassstm"]
old-location: stg\writeclassstm.htm
tech.root: Stg
ms.assetid: c08bfbc8-f7ac-4534-8c98-c732c6daa2f7
ms.date: 12/05/2018
ms.keywords: WriteClassStm, WriteClassStm function [Structured Storage], _stg_writeclassstm, coml2api/WriteClassStm, stg.writeclassstm
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
 - WriteClassStm
 - coml2api/WriteClassStm
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
 - WriteClassStm
---

# WriteClassStm function


## -description

The <b>WriteClassStm</b> function stores the specified CLSID in the stream.

## -parameters

### -param pStm [in]

<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> pointer to the stream into which the CLSID is to be written.

### -param rclsid [in]

Specifies the CLSID to write to the stream.

## -returns

This function returns HRESULT.

## -remarks

The 
<b>WriteClassStm</b> function writes a CLSID to the specified stream object so it can be read by the 
<a href="/windows/desktop/api/coml2api/nf-coml2api-readclassstm">ReadClassStm</a> function. Most applications do not call 
<b>WriteClassStm</b> directly. OLE calls it before making a call to an object's 
<a href="/windows/desktop/api/objidl/nf-objidl-ipersiststream-save">IPersistStream::Save</a> method.

## -see-also

<a href="/windows/desktop/api/coml2api/nf-coml2api-readclassstg">ReadClassStg</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-readclassstm">ReadClassStm</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstg">WriteClassStg</a>