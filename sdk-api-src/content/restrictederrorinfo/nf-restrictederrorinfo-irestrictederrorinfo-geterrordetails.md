---
UID: NF:restrictederrorinfo.IRestrictedErrorInfo.GetErrorDetails
title: IRestrictedErrorInfo::GetErrorDetails (restrictederrorinfo.h)
description: Returns information about an error, including the restricted error description.
helpviewer_keywords: ["GetErrorDetails","GetErrorDetails method [Windows Runtime]","GetErrorDetails method [Windows Runtime]","IRestrictedErrorInfo interface","IRestrictedErrorInfo interface [Windows Runtime]","GetErrorDetails method","IRestrictedErrorInfo.GetErrorDetails","IRestrictedErrorInfo::GetErrorDetails","restrictederrorinfo/IRestrictedErrorInfo::GetErrorDetails","winrt.irestrictederrorinfo_geterrordetails"]
old-location: winrt\irestrictederrorinfo_geterrordetails.htm
tech.root: WinRT
ms.assetid: ecfd97cf-9f8f-4940-9499-a894e0883f04
ms.date: 12/05/2018
ms.keywords: GetErrorDetails, GetErrorDetails method [Windows Runtime], GetErrorDetails method [Windows Runtime],IRestrictedErrorInfo interface, IRestrictedErrorInfo interface [Windows Runtime],GetErrorDetails method, IRestrictedErrorInfo.GetErrorDetails, IRestrictedErrorInfo::GetErrorDetails, restrictederrorinfo/IRestrictedErrorInfo::GetErrorDetails, winrt.irestrictederrorinfo_geterrordetails
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
 - IRestrictedErrorInfo::GetErrorDetails
 - restrictederrorinfo/IRestrictedErrorInfo::GetErrorDetails
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
 - IRestrictedErrorInfo.GetErrorDetails
---

# IRestrictedErrorInfo::GetErrorDetails


## -description

Returns information about an error, including the restricted error description.

## -parameters

### -param description [out]

Type: <b>BSTR*</b>

The error description.

### -param error [out]

Type: <b>HRESULT*</b>

The error code associated with the error condition.

### -param restrictedDescription [out]

Type: <b>BSTR*</b>

The restricted error description.

### -param capabilitySid

TBD

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a>