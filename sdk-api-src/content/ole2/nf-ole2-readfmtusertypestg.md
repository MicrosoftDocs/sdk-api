---
UID: NF:ole2.ReadFmtUserTypeStg
title: ReadFmtUserTypeStg function (ole2.h)
description: The ReadFmtUserTypeStg function returns the clipboard format and user type previously saved with the WriteFmtUserTypeStg function.
helpviewer_keywords: ["ReadFmtUserTypeStg","ReadFmtUserTypeStg function [Structured Storage]","_stg_readfmtusertypestg","ole2/ReadFmtUserTypeStg","stg.readfmtusertypestg"]
old-location: stg\readfmtusertypestg.htm
tech.root: Stg
ms.assetid: 6f26550d-c094-4150-b8ef-2da1d052c1ff
ms.date: 12/05/2018
ms.keywords: ReadFmtUserTypeStg, ReadFmtUserTypeStg function [Structured Storage], _stg_readfmtusertypestg, ole2/ReadFmtUserTypeStg, stg.readfmtusertypestg
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ReadFmtUserTypeStg
 - ole2/ReadFmtUserTypeStg
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - ext-ms-win-com-ole32-l1-1-4.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ole32.dll
api_name:
 - ReadFmtUserTypeStg
---

# ReadFmtUserTypeStg function


## -description

The 
<b>ReadFmtUserTypeStg</b> function returns the clipboard format and user type previously saved with the 
<a href="/windows/desktop/api/ole2/nf-ole2-writefmtusertypestg">WriteFmtUserTypeStg</a> function.

## -parameters

### -param pstg [in]

Pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on the storage object from which the information is to be read.

### -param pcf [out]

Pointer to where the clipboard format is to be written on return. It can be <b>NULL</b>, indicating the format is of no interest to the caller.

### -param lplpszUserType [out]

Address of <b>LPWSTR</b> pointer variable that receives a pointer to the null-terminated Unicode user-type string. The caller can specify <b>NULL</b> for this parameter, which indicates that the user type is of no interest. This function allocates memory for the string. The caller is responsible for freeing the memory with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

This function supports the standard return values E_FAIL, E_INVALIDARG, and E_OUTOFMEMORY, in addition to the following:

This function also returns any of the error values returned by the 
<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> method.

## -remarks

<b>ReadFmtUserTypeStg</b> returns the clipboard format and the user type string from the specified storage object. The 
<a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstg">WriteClassStg</a> function must have been called before calling the 
<b>ReadFmtUserTypeStg</b> function.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>



<a href="/windows/desktop/api/ole2/nf-ole2-writefmtusertypestg">WriteFmtUserTypeStg</a>