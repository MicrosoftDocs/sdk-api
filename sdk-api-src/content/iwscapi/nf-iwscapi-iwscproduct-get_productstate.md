---
UID: NF:iwscapi.IWscProduct.get_ProductState
title: IWscProduct::get_ProductState
author: windows-sdk-content
description: Returns the current state of the signature data for the security product.
old-location: winprog\iwscproduct_productstate.htm
tech.root: devnotes
ms.assetid: 73E4EA93-C298-4F25-BC51-DB6E38B48EE3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWscProduct interface [Windows API],get_ProductState method, IWscProduct.get_ProductState, IWscProduct::get_ProductState, get_ProductState, get_ProductState method [Windows API], get_ProductState method [Windows API],IWscProduct interface, iwscapi/IWscProduct::get_ProductState, winprog.iwscproduct_productstate
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
 - IWscProduct.get_ProductState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWscProduct::get_ProductState


## -description


Returns the current state of the signature data for the security product.


## -parameters




### -param pVal [out]

A pointer to the state value of the signature of the security product. 


## -returns



If the method  succeeds, returns S_OK.

If the method  fails, returns a Win32 error code.




## -see-also




<a href="https://msdn.microsoft.com/C637E67A-CED7-4235-AAF3-22730E9C7E91">IWscProduct</a>
 

 

