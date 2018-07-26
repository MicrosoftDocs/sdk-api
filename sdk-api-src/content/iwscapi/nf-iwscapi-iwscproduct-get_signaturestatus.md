---
UID: NF:iwscapi.IWscProduct.get_SignatureStatus
title: IWscProduct::get_SignatureStatus
author: windows-sdk-content
description: Returns the current status of the signature data for the security product.
old-location: winprog\iwscproduct_signaturestatus.htm
old-project: devnotes
ms.assetid: 07F7EADE-44E9-472F-BA30-7B7EDEF48192
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IWscProduct interface [Windows API],get_SignatureStatus method, IWscProduct.get_SignatureStatus, IWscProduct::get_SignatureStatus, get_SignatureStatus, get_SignatureStatus method [Windows API], get_SignatureStatus method [Windows API],IWscProduct interface, iwscapi/IWscProduct::get_SignatureStatus, winprog.iwscproduct_signaturestatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WSC_SECURITY_SIGNATURE_STATUS
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
req.lib: Wscapi.lib
req.dll: Wscapi.dll
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/C637E67A-CED7-4235-AAF3-22730E9C7E91">IWscProduct</a>
 

 

