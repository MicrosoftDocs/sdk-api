---
UID: NF:restrictederrorinfo.IRestrictedErrorInfo.GetReference
title: IRestrictedErrorInfo::GetReference (restrictederrorinfo.h)
description: Returns a reference to restricted error information.
helpviewer_keywords: ["GetReference","GetReference method [Windows Runtime]","GetReference method [Windows Runtime]","IRestrictedErrorInfo interface","IRestrictedErrorInfo interface [Windows Runtime]","GetReference method","IRestrictedErrorInfo.GetReference","IRestrictedErrorInfo::GetReference","restrictederrorinfo/IRestrictedErrorInfo::GetReference","winrt.irestrictederrorinfo_getreference"]
old-location: winrt\irestrictederrorinfo_getreference.htm
tech.root: WinRT
ms.assetid: e7f0c451-c6a4-49ec-a97a-dc834081b3c1
ms.date: 12/05/2018
ms.keywords: GetReference, GetReference method [Windows Runtime], GetReference method [Windows Runtime],IRestrictedErrorInfo interface, IRestrictedErrorInfo interface [Windows Runtime],GetReference method, IRestrictedErrorInfo.GetReference, IRestrictedErrorInfo::GetReference, restrictederrorinfo/IRestrictedErrorInfo::GetReference, winrt.irestrictederrorinfo_getreference
req.header: restrictederrorinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RestrictedErrorInfo.idl
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
 - IRestrictedErrorInfo::GetReference
 - restrictederrorinfo/IRestrictedErrorInfo::GetReference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RestrictedErrorInfo.h
api_name:
 - IRestrictedErrorInfo.GetReference
---

# IRestrictedErrorInfo::GetReference


## -description

Returns a reference to restricted error information.

## -parameters

### -param reference [out]

Type: <b>BSTR*</b>

A reference to the error information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a>