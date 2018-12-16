---
UID: NF:iwscapi.IWscProduct.get_RemediationPath
title: IWscProduct::get_RemediationPath
author: windows-sdk-content
description: Returns the current remediation path for the security product.
old-location: winprog\iwscproduct_remediationpath.htm
tech.root: devnotes
ms.assetid: 6922B572-4E00-4B0B-BE1F-64343DD776A0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWscProduct interface [Windows API],get_RemediationPath method, IWscProduct.get_RemediationPath, IWscProduct::get_RemediationPath, get_RemediationPath, get_RemediationPath method [Windows API], get_RemediationPath method [Windows API],IWscProduct interface, iwscapi/IWscProduct::get_RemediationPath, winprog.iwscproduct_remediationpath
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
 - IWscProduct.get_RemediationPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWscProduct::get_RemediationPath


## -description


Returns the current remediation path for the security product.


## -parameters




### -param pVal [out]

A pointer to the remediation path for the security product. This is displayed in the Windows Security Center user interface.


## -returns



If the method  succeeds, returns S_OK.

If the method  fails, returns a Win32 error code.




## -see-also




<a href="https://msdn.microsoft.com/C637E67A-CED7-4235-AAF3-22730E9C7E91">IWscProduct</a>
 

 

