---
UID: NF:restrictederrorinfo.ILanguageExceptionErrorInfo2.GetPropagationContextHead
title: ILanguageExceptionErrorInfo2::GetPropagationContextHead (restrictederrorinfo.h)
description: Retrieves the propagation context head.
helpviewer_keywords: ["GetPropagationContextHead","GetPropagationContextHead method [Windows Runtime]","GetPropagationContextHead method [Windows Runtime]","ILanguageExceptionErrorInfo2 interface","ILanguageExceptionErrorInfo2 interface [Windows Runtime]","GetPropagationContextHead method","ILanguageExceptionErrorInfo2.GetPropagationContextHead","ILanguageExceptionErrorInfo2::GetPropagationContextHead","restrictederrorinfo/ILanguageExceptionErrorInfo2::GetPropagationContextHead","winrt.ilanguageexceptionerrorinfo2_getpropagationcontexthead"]
old-location: winrt\ilanguageexceptionerrorinfo2_getpropagationcontexthead.htm
tech.root: WinRT
ms.assetid: 1E5C74AE-C8C6-4D95-A836-DD47E50CF25D
ms.date: 12/05/2018
ms.keywords: GetPropagationContextHead, GetPropagationContextHead method [Windows Runtime], GetPropagationContextHead method [Windows Runtime],ILanguageExceptionErrorInfo2 interface, ILanguageExceptionErrorInfo2 interface [Windows Runtime],GetPropagationContextHead method, ILanguageExceptionErrorInfo2.GetPropagationContextHead, ILanguageExceptionErrorInfo2::GetPropagationContextHead, restrictederrorinfo/ILanguageExceptionErrorInfo2::GetPropagationContextHead, winrt.ilanguageexceptionerrorinfo2_getpropagationcontexthead
req.header: restrictederrorinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Restrictederrorinfo.idl
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
 - ILanguageExceptionErrorInfo2::GetPropagationContextHead
 - restrictederrorinfo/ILanguageExceptionErrorInfo2::GetPropagationContextHead
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - restrictederrorinfo.h
api_name:
 - ILanguageExceptionErrorInfo2.GetPropagationContextHead
---

# ILanguageExceptionErrorInfo2::GetPropagationContextHead


## -description

Retrieves the propagation context head.

## -parameters

### -param propagatedLanguageExceptionErrorInfoHead [out]

On success, returns an <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo2">ILanguageExceptionErrorInfo2</a> object that represents the head of the propagation context.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can use <b>GetPropagationContextHead</b> to retrieve the linked list of <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> objects that contains additional error information on the exception in question. You can then use <a href="/windows/desktop/api/restrictederrorinfo/nf-restrictederrorinfo-ilanguageexceptionerrorinfo2-getpreviouslanguageexceptionerrorinfo">GetPreviousLanguageExceptionErrorInfo</a> to move through that linked list, and examine each error separately.

 The operating system also uses this method to retrieve the stored exceptions associated with the error.

## -see-also

<a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo2">ILanguageExceptionErrorInfo2</a>