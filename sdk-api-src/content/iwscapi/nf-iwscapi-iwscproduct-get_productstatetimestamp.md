---
UID: NF:iwscapi.IWscProduct.get_ProductStateTimestamp
title: IWscProduct::get_ProductStateTimestamp (iwscapi.h)

description: Returns the current time stamp for the security product.
old-location: winprog\iwscproduct_producttimestamp.htm
tech.root: DevNotes
ms.assetid: 3BE70437-8BBE-47DF-8C5E-390353073580

ms.date: 12/05/2018
ms.keywords: IWscProduct interface [Windows API],get_ProductStateTimeStamp method, IWscProduct.get_ProductStateTimestamp, IWscProduct::get_ProductStateTimeStamp, IWscProduct::get_ProductStateTimestamp, get_ProductStateTimeStamp, get_ProductStateTimeStamp method [Windows API], get_ProductStateTimeStamp method [Windows API],IWscProduct interface, get_ProductStateTimestamp, iwscapi/IWscProduct::get_ProductStateTimeStamp, winprog.iwscproduct_producttimestamp
ms.topic: method
f1_keywords: 
 - "iwscapi/IWscProduct.get_ProductStateTimeStamp"
dev_langs:
 - c++
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
 - IWscProduct.get_ProductStateTimeStamp
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWscProduct::get_ProductStateTimestamp


## -description


Returns the current time  stamp for the security product.


## -parameters




### -param pVal [out]

A pointer to the time stamp of the security product. This is displayed in the Windows Security Center user interface.


## -returns



If the method  succeeds, returns S_OK.

If the method  fails, returns a Win32 error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iwscapi/nn-iwscapi-iwscproduct">IWscProduct</a>
 

 

