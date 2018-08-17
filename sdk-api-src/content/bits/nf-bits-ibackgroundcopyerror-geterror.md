---
UID: NF:bits.IBackgroundCopyError.GetError
title: IBackgroundCopyError::GetError
author: windows-sdk-content
description: Retrieves the error code and identify the context in which the error occurred.
old-location: bits\ibackgroundcopyerror_geterror.htm
old-project: bits
ms.assetid: abdf115d-3ff2-4664-b053-f55872ad24ab
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetError, GetError method [BITS], GetError method [BITS],IBackgroundCopyError interface, IBackgroundCopyError interface [BITS],GetError method, IBackgroundCopyError.GetError, IBackgroundCopyError::GetError, _drz_ibackgroundcopyerror_geterror, bits.ibackgroundcopyerror_geterror, bits/IBackgroundCopyError::GetError
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyError.GetError
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyError::GetError


## -description


Retrieves the error code and identify the context in which the error occurred.


## -parameters




### -param pContext [out]

Context in which the error occurred. For a list of context values, see the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362798(v=VS.85).aspx">BG_ERROR_CONTEXT</a> enumeration.


### -param pCode






#### - pErrorCode [out]

Error code of the error that occurred.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM HRESULT values on error.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362877(v=VS.85).aspx">IBackgroundCopyError::GetErrorContextDescription</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362878(v=VS.85).aspx">IBackgroundCopyError::GetErrorDescription</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362879(v=VS.85).aspx">IBackgroundCopyError::GetFile</a>
 

 

