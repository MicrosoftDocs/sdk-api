---
UID: NF:restrictederrorinfo.IRestrictedErrorInfo.GetErrorDetails
title: IRestrictedErrorInfo::GetErrorDetails
author: windows-sdk-content
description: Returns information about an error, including the restricted error description.
old-location: winrt\irestrictederrorinfo_geterrordetails.htm
tech.root: WinRT
ms.assetid: ecfd97cf-9f8f-4940-9499-a894e0883f04
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetErrorDetails, GetErrorDetails method [Windows Runtime], GetErrorDetails method [Windows Runtime],IRestrictedErrorInfo interface, IRestrictedErrorInfo interface [Windows Runtime],GetErrorDetails method, IRestrictedErrorInfo.GetErrorDetails, IRestrictedErrorInfo::GetErrorDetails, restrictederrorinfo/IRestrictedErrorInfo::GetErrorDetails, winrt.irestrictederrorinfo_geterrordetails
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RestrictedErrorInfo.h
api_name:
 - IRestrictedErrorInfo.GetErrorDetails
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- restrictederrorinfo.h
: 
- IRestrictedErrorInfo.GetErrorDetails
: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a>
 

 

