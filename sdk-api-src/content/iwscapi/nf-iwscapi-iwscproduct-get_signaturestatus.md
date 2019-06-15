---
UID: NF:iwscapi.IWscProduct.get_SignatureStatus
title: IWscProduct::get_SignatureStatus (iwscapi.h)
author: windows-sdk-content
description: Returns the current status of the signature data for the security product.
old-location: winprog\iwscproduct_signaturestatus.htm
tech.root: DevNotes
ms.assetid: 07F7EADE-44E9-472F-BA30-7B7EDEF48192
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWscProduct interface [Windows API],get_SignatureStatus method, IWscProduct.get_SignatureStatus, IWscProduct::get_SignatureStatus, get_SignatureStatus, get_SignatureStatus method [Windows API], get_SignatureStatus method [Windows API],IWscProduct interface, iwscapi/IWscProduct::get_SignatureStatus, winprog.iwscproduct_signaturestatus
ms.topic: method
f1_keywords: ["iwscapi/IWscProduct.get_SignatureStatus"]
req.header: iwscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wscapi.lib
req.dll: Wscapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wscapi.dll
api_name:
 - IWscProduct.get_SignatureStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWscProduct::get_SignatureStatus


## -description


Returns the current status of the signature data for the security product.


## -parameters




### -param pVal [out]

A pointer to the status value of the signature of the security product. If the security product is a Firewall product, the return value is always <b>WSC_SECURITY_PRODUCT_UP_TO_DATE</b> because firewalls do not contain signature data.


## -returns



If the method  succeeds, returns S_OK.

If the method  fails, returns a Win32 error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iwscapi/nn-iwscapi-iwscproduct">IWscProduct</a>
 

 

