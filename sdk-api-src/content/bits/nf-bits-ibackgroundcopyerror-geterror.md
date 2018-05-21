---
UID: NF:bits.IBackgroundCopyError.GetError
title: IBackgroundCopyError::GetError
author: windows-driver-content
description: Retrieves the error code and identify the context in which the error occurred.
old-location: bits\ibackgroundcopyerror_geterror.htm
old-project: Bits
ms.assetid: abdf115d-3ff2-4664-b053-f55872ad24ab
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: GetError, GetError method [BITS], GetError method [BITS],IBackgroundCopyError interface, IBackgroundCopyError interface [BITS],GetError method, IBackgroundCopyError.GetError, IBackgroundCopyError::GetError, _drz_ibackgroundcopyerror_geterror, bits.ibackgroundcopyerror_geterror, bits/IBackgroundCopyError::GetError
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits.h
req.include-header: 
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
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IBackgroundCopyError.GetError
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
<a href="https://msdn.microsoft.com/c9d98518-6f2e-4fd1-b0ee-6735c6d6ecd9">BG_ERROR_CONTEXT</a> enumeration.


### -param pCode






#### - pErrorCode [out]

Error code of the error that occurred.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM HRESULT values on error.




## -see-also




<a href="https://msdn.microsoft.com/87f5ae62-c171-4637-bebb-3a5c5aa546b3">IBackgroundCopyError::GetErrorContextDescription</a>



<a href="https://msdn.microsoft.com/57323f38-c2e6-4e40-b357-7df758899f97">IBackgroundCopyError::GetErrorDescription</a>



<a href="https://msdn.microsoft.com/7b6d4bd4-2102-4e6b-b250-1d73fae94cf9">IBackgroundCopyError::GetFile</a>
 

 

