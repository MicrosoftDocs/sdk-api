---
UID: NF:oaidl.IErrorInfo.GetSource
title: IErrorInfo::GetSource (oaidl.h)
description: Returns the language-dependent programmatic ID (ProgID) for the class or application that raised the error.
helpviewer_keywords: ["GetSource","GetSource method [Automation]","GetSource method [Automation]","IErrorInfo interface","IErrorInfo interface [Automation]","GetSource method","IErrorInfo.GetSource","IErrorInfo::GetSource","_oa96_IErrorInfo_GetSource","automat.ierrorinfo_getsource","oaidl/IErrorInfo::GetSource"]
old-location: automat\ierrorinfo_getsource.htm
tech.root: automat
ms.assetid: b7bbf4ac-7c02-4abe-83fb-bc9fcd52129e
ms.date: 12/05/2018
ms.keywords: GetSource, GetSource method [Automation], GetSource method [Automation],IErrorInfo interface, IErrorInfo interface [Automation],GetSource method, IErrorInfo.GetSource, IErrorInfo::GetSource, _oa96_IErrorInfo_GetSource, automat.ierrorinfo_getsource, oaidl/IErrorInfo::GetSource
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - IErrorInfo::GetSource
 - oaidl/IErrorInfo::GetSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - IErrorInfo.GetSource
---

# IErrorInfo::GetSource


## -description

Returns the language-dependent programmatic ID (ProgID) for the class or application that raised the error.

## -parameters

### -param pBstrSource [out]

A ProgID, in the form <i>progname</i>.<i>objectname</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use <b>IErrorInfo::GetSource</b> to determine the class or application that is the source of the error. The language for the returned ProgID depends on the locale ID (LCID) that was passed into the method at the time of invocation.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo">IErrorInfo</a>