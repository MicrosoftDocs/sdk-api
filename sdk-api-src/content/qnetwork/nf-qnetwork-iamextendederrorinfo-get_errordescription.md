---
UID: NF:qnetwork.IAMExtendedErrorInfo.get_ErrorDescription
title: IAMExtendedErrorInfo::get_ErrorDescription
author: windows-sdk-content
description: The get_ErrorDescription method retrieves the extended error description.
old-location: dshow\iamextendederrorinfo_get_errordescription.htm
old-project: DirectShow
ms.assetid: d417855e-7df6-4978-b971-a91b79c5fa2c
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMExtendedErrorInfo interface [DirectShow],get_ErrorDescription method, IAMExtendedErrorInfo.get_ErrorDescription, IAMExtendedErrorInfo::get_ErrorDescription, IAMExtendedErrorInfoget_ErrorDescription, dshow.iamextendederrorinfo_get_errordescription, get_ErrorDescription, get_ErrorDescription method [DirectShow], get_ErrorDescription method [DirectShow],IAMExtendedErrorInfo interface, qnetwork/IAMExtendedErrorInfo::get_ErrorDescription
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: AMExtendedSeekingCapabilities
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMExtendedErrorInfo.get_ErrorDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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




<a href="https://msdn.microsoft.com/0e3274e6-7c22-4175-8b2e-cdf4afc1225e">IAMExtendedErrorInfo Interface</a>
 

 

