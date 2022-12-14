---
UID: NF:restrictederrorinfo.ILanguageExceptionErrorInfo2.GetPreviousLanguageExceptionErrorInfo
title: ILanguageExceptionErrorInfo2::GetPreviousLanguageExceptionErrorInfo (restrictederrorinfo.h)
description: Retrieves the previous language exception error information object.
helpviewer_keywords: ["GetPreviousLanguageExceptionErrorInfo","GetPreviousLanguageExceptionErrorInfo method [Windows Runtime]","GetPreviousLanguageExceptionErrorInfo method [Windows Runtime]","ILanguageExceptionErrorInfo2 interface","ILanguageExceptionErrorInfo2 interface [Windows Runtime]","GetPreviousLanguageExceptionErrorInfo method","ILanguageExceptionErrorInfo2.GetPreviousLanguageExceptionErrorInfo","ILanguageExceptionErrorInfo2::GetPreviousLanguageExceptionErrorInfo","restrictederrorinfo/ILanguageExceptionErrorInfo2::GetPreviousLanguageExceptionErrorInfo","winrt.ilanguageexceptionerrorinfo2_getpreviouslanguageexceptionerrorinfo"]
old-location: winrt\ilanguageexceptionerrorinfo2_getpreviouslanguageexceptionerrorinfo.htm
tech.root: WinRT
ms.assetid: 10A45EF1-AF8F-498D-B95B-FCE9EF8AB203
ms.date: 12/05/2018
ms.keywords: GetPreviousLanguageExceptionErrorInfo, GetPreviousLanguageExceptionErrorInfo method [Windows Runtime], GetPreviousLanguageExceptionErrorInfo method [Windows Runtime],ILanguageExceptionErrorInfo2 interface, ILanguageExceptionErrorInfo2 interface [Windows Runtime],GetPreviousLanguageExceptionErrorInfo method, ILanguageExceptionErrorInfo2.GetPreviousLanguageExceptionErrorInfo, ILanguageExceptionErrorInfo2::GetPreviousLanguageExceptionErrorInfo, restrictederrorinfo/ILanguageExceptionErrorInfo2::GetPreviousLanguageExceptionErrorInfo, winrt.ilanguageexceptionerrorinfo2_getpreviouslanguageexceptionerrorinfo
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
 - ILanguageExceptionErrorInfo2::GetPreviousLanguageExceptionErrorInfo
 - restrictederrorinfo/ILanguageExceptionErrorInfo2::GetPreviousLanguageExceptionErrorInfo
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
 - ILanguageExceptionErrorInfo2.GetPreviousLanguageExceptionErrorInfo
---

# ILanguageExceptionErrorInfo2::GetPreviousLanguageExceptionErrorInfo


## -description

Retrieves the previous language exception error information object.

## -parameters

### -param previousLanguageExceptionErrorInfo [out]

Pointer to an <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo2">ILanguageExceptionErrorInfo2</a> object that contains the previous error information object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Generally speaking, <a href="/windows/desktop/api/restrictederrorinfo/nf-restrictederrorinfo-ilanguageexceptionerrorinfo2-getpropagationcontexthead">GetPropagationContextHead</a> is utilized to retrieve the linked list of <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> objects that contains additional error information on the exception in question. You can then use <b>GetPreviousLanguageExceptionErrorInfo</b> to move through that linked list, and examine each error separately.


The operating system also uses this method to retrieve the stored exceptions associated with the error.

## -see-also

<a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo2">ILanguageExceptionErrorInfo2</a>