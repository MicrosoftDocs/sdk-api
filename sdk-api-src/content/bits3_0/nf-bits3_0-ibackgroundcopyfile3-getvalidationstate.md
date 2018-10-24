---
UID: NF:bits3_0.IBackgroundCopyFile3.GetValidationState
title: IBackgroundCopyFile3::GetValidationState
author: windows-sdk-content
description: Gets the current validation state of this file.
old-location: bits\ibackgroundcopyfile3_getvalidationstate.htm
tech.root: Bits
ms.assetid: 705644e2-fd15-4225-b26a-e75c2dd2f6e3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetValidationState, GetValidationState method [BITS], GetValidationState method [BITS],IBackgroundCopyFile3 interface, IBackgroundCopyFile3 interface [BITS],GetValidationState method, IBackgroundCopyFile3.GetValidationState, IBackgroundCopyFile3::GetValidationState, bits.ibackgroundcopyfile3_getvalidationstate, bits3_0/IBackgroundCopyFile3::GetValidationState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
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
req.lib: Bits.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
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



Note that <b>FALSE</b> may not mean that the file is not valid, it may mean the <a href="https://msdn.microsoft.com/c032ce32-07a4-4ab2-ae57-f9d526d1371a">IBackgroundCopyFile3::SetValidationState</a> has not been called.




## -see-also




<a href="https://msdn.microsoft.com/5304f93a-993a-4327-9fdb-fb2ef1dafecb">IBackgroundCopyFile3</a>



<a href="https://msdn.microsoft.com/c032ce32-07a4-4ab2-ae57-f9d526d1371a">IBackgroundCopyFile3::SetValidationState</a>



<a href="https://msdn.microsoft.com/f492f009-bef7-412e-8626-ae84cd5ce03f">IBitsPeerCacheRecord::IsFileValidated</a>
 

 

