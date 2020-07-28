---
UID: NF:qnetwork.IAMExtendedErrorInfo.get_ErrorDescription
title: IAMExtendedErrorInfo::get_ErrorDescription (qnetwork.h)
description: The get_ErrorDescription method retrieves the extended error description.
helpviewer_keywords: ["IAMExtendedErrorInfo interface [DirectShow]","get_ErrorDescription method","IAMExtendedErrorInfo.get_ErrorDescription","IAMExtendedErrorInfo::get_ErrorDescription","IAMExtendedErrorInfoget_ErrorDescription","dshow.iamextendederrorinfo_get_errordescription","get_ErrorDescription","get_ErrorDescription method [DirectShow]","get_ErrorDescription method [DirectShow]","IAMExtendedErrorInfo interface","qnetwork/IAMExtendedErrorInfo::get_ErrorDescription"]
old-location: dshow\iamextendederrorinfo_get_errordescription.htm
tech.root: dshow
ms.assetid: d417855e-7df6-4978-b971-a91b79c5fa2c
ms.date: 12/05/2018
ms.keywords: IAMExtendedErrorInfo interface [DirectShow],get_ErrorDescription method, IAMExtendedErrorInfo.get_ErrorDescription, IAMExtendedErrorInfo::get_ErrorDescription, IAMExtendedErrorInfoget_ErrorDescription, dshow.iamextendederrorinfo_get_errordescription, get_ErrorDescription, get_ErrorDescription method [DirectShow], get_ErrorDescription method [DirectShow],IAMExtendedErrorInfo interface, qnetwork/IAMExtendedErrorInfo::get_ErrorDescription
f1_keywords:
- qnetwork/IAMExtendedErrorInfo.get_ErrorDescription
dev_langs:
- c++
req.header: qnetwork.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Qnetwork.h
api_name:
- IAMExtendedErrorInfo.get_ErrorDescription
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMExtendedErrorInfo::get_ErrorDescription


## -description



The <code>get_ErrorDescription</code> method retrieves the extended error description.




## -parameters




### -param pbstrErrorDescription [out]

Pointer to a variable that receives the error description.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nn-qnetwork-iamextendederrorinfo">IAMExtendedErrorInfo Interface</a>
 

 

