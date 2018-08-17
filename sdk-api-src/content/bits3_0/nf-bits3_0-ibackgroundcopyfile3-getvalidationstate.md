---
UID: NF:bits3_0.IBackgroundCopyFile3.GetValidationState
title: IBackgroundCopyFile3::GetValidationState
author: windows-sdk-content
description: Gets the current validation state of this file.
old-location: bits\ibackgroundcopyfile3_getvalidationstate.htm
old-project: bits
ms.assetid: 705644e2-fd15-4225-b26a-e75c2dd2f6e3
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetValidationState, GetValidationState method [BITS], GetValidationState method [BITS],IBackgroundCopyFile3 interface, IBackgroundCopyFile3 interface [BITS],GetValidationState method, IBackgroundCopyFile3.GetValidationState, IBackgroundCopyFile3::GetValidationState, bits.ibackgroundcopyfile3_getvalidationstate, bits3_0/IBackgroundCopyFile3::GetValidationState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyFile3.GetValidationState
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBackgroundCopyFile3::GetValidationState


## -description


Gets the current validation state of this file.


## -parameters




### -param pState [out]

<b>TRUE</b> if the contents of the file is valid, otherwise, <b>FALSE</b>.


## -returns



The method returns the following return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



Note that <b>FALSE</b> may not mean that the file is not valid, it may mean the <a href="https://msdn.microsoft.com/en-us/library/Aa362955(v=VS.85).aspx">IBackgroundCopyFile3::SetValidationState</a> has not been called.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362952(v=VS.85).aspx">IBackgroundCopyFile3</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362955(v=VS.85).aspx">IBackgroundCopyFile3::SetValidationState</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964298(v=VS.85).aspx">IBitsPeerCacheRecord::IsFileValidated</a>
 

 

