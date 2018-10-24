---
UID: NF:imm.ImmGetCandidateListA
title: ImmGetCandidateListA function
author: windows-sdk-content
description: Retrieves a candidate list.
old-location: intl\immgetcandidatelist.htm
tech.root: Intl
ms.assetid: 24163117-a283-4067-8ce6-118ca2de62c9
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ImmGetCandidateList, ImmGetCandidateList function [Internationalization for Windows Applications], ImmGetCandidateListA, ImmGetCandidateListW, _win32_ImmGetCandidateList, imm/ImmGetCandidateList, imm/ImmGetCandidateListA, imm/ImmGetCandidateListW, intl.immgetcandidatelist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmGetCandidateListW (Unicode) and ImmGetCandidateListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - imm32.dll
api_name:
 - ImmGetCandidateList
 - ImmGetCandidateListA
 - ImmGetCandidateListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmGetCandidateListA function


## -description


Retrieves a candidate list.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param deIndex [in]

Zero-based index of the candidate list.


### -param lpCandList [out, optional]

Pointer to a <a href="https://msdn.microsoft.com/d60b28fb-0cdd-43b4-8d99-cb829bea6679">CANDIDATELIST</a> structure in which the function retrieves the candidate list.


### -param dwBufLen [in]

Size, in bytes, of the buffer to receive the candidate list. The application can specify 0 for this parameter if the function is to return the required size of the output buffer only.


## -returns



Returns the number of bytes copied to the candidate list buffer if successful. If the application has supplied 0 for the <i>dwBufLen</i> parameter, the function returns the size required for the candidate list buffer.

The function returns 0 if it does not succeed.




## -see-also




<a href="https://msdn.microsoft.com/d60b28fb-0cdd-43b4-8d99-cb829bea6679">CANDIDATELIST</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

