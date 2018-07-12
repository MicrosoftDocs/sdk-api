---
UID: NF:bits.IEnumBackgroundCopyFiles.GetCount
title: IEnumBackgroundCopyFiles::GetCount
author: windows-sdk-content
description: Retrieves a count of the number of files in the enumeration.
old-location: bits\ienumbackgroundcopyfiles_getcount.htm
old-project: bits
ms.assetid: 24a9d5f9-e923-4b20-8abf-8ce50fc2602b
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: GetCount, GetCount method [BITS], GetCount method [BITS],IEnumBackgroundCopyFiles interface, IEnumBackgroundCopyFiles interface [BITS],GetCount method, IEnumBackgroundCopyFiles.GetCount, IEnumBackgroundCopyFiles::GetCount, _drz_ienumbackgroundcopyfiles_getcount, bits.ienumbackgroundcopyfiles_getcount, bits/IEnumBackgroundCopyFiles::GetCount
ms.prod: windows
ms.technology: windows-sdk
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
 - IEnumBackgroundCopyFiles.GetCount
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IEnumBackgroundCopyFiles::GetCount


## -description


Retrieves a count of the number of files in the enumeration.


## -parameters




### -param puCount






#### - pCount [out]

Number of files in the enumeration.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://msdn.microsoft.com/831998ba-601c-43c4-ba27-faff741f8eb4">IEnumBackgroundCopyFiles</a>
 

 

