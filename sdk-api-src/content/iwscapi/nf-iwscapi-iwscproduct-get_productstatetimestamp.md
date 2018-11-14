---
UID: NF:iwscapi.IWscProduct.get_ProductStateTimestamp
title: IWscProduct::get_ProductStateTimestamp
author: windows-sdk-content
description: Returns the current time stamp for the security product.
old-location: winprog\iwscproduct_producttimestamp.htm
tech.root: devnotes
ms.assetid: 3BE70437-8BBE-47DF-8C5E-390353073580
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IWscProduct interface [Windows API],get_ProductStateTimeStamp method, IWscProduct.get_ProductStateTimestamp, IWscProduct::get_ProductStateTimeStamp, IWscProduct::get_ProductStateTimestamp, get_ProductStateTimeStamp, get_ProductStateTimeStamp method [Windows API], get_ProductStateTimeStamp method [Windows API],IWscProduct interface, get_ProductStateTimestamp, iwscapi/IWscProduct::get_ProductStateTimeStamp, winprog.iwscproduct_producttimestamp
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- iwscapi.h
: 
- IWscProduct.get_ProductStateTimestamp
: 
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




<a href="https://msdn.microsoft.com/C637E67A-CED7-4235-AAF3-22730E9C7E91">IWscProduct</a>
 

 

