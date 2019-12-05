---
UID: NF:oaidl.IErrorInfo.GetDescription
title: IErrorInfo::GetDescription (oaidl.h)
description: Returns a textual description of the error.
old-location: automat\ierrorinfo_getdescription.htm
tech.root: automat
ms.assetid: 672884a8-4dfc-473c-a13d-d1723fcd01cb
ms.date: 12/05/2018
ms.keywords: GetDescription, GetDescription method [Automation], GetDescription method [Automation],IErrorInfo interface, IErrorInfo interface [Automation],GetDescription method, IErrorInfo.GetDescription, IErrorInfo::GetDescription, _oa96_IErrorInfo_GetDescription, automat.ierrorinfo_getdescription, oaidl/IErrorInfo::GetDescription
ms.topic: method
f1_keywords:
- oaidl/IErrorInfo.GetDescription
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- oaidl.h
api_name:
- IErrorInfo.GetDescription
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IErrorInfo::GetDescription


## -description


  Returns a textual description of the error.


## -parameters




### -param pBstrDescription [out]

A brief description of the error.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The text is returned in the language specified by the locale identifier (LCID) that was passed to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">IDispatch::Invoke</a> for the method that encountered the error.





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo">IErrorInfo</a>
 

 

