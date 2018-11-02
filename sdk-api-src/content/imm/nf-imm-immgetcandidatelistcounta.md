---
UID: NF:imm.ImmGetCandidateListCountA
title: ImmGetCandidateListCountA function
author: windows-sdk-content
description: Retrieves the size of the candidate lists.
old-location: intl\immgetcandidatelistcount.htm
tech.root: Intl
ms.assetid: da7c4eee-3c79-4ea8-b9a5-3b43befa0021
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ImmGetCandidateListCount, ImmGetCandidateListCount function [Internationalization for Windows Applications], ImmGetCandidateListCountA, ImmGetCandidateListCountW, _win32_ImmGetCandidateListCount, imm/ImmGetCandidateListCount, imm/ImmGetCandidateListCountA, imm/ImmGetCandidateListCountW, intl.immgetcandidatelistcount
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
req.unicode-ansi: ImmGetCandidateListCountW (Unicode) and ImmGetCandidateListCountA (ANSI)
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
 - Imm32.dll
api_name:
 - ImmGetCandidateListCount
 - ImmGetCandidateListCountA
 - ImmGetCandidateListCountW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmGetCandidateListCountA function


## -description


Retrieves the size of the candidate lists.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param lpdwListCount [out]

Pointer to the buffer in which this function retrieves the size of the candidate lists.


## -returns



Returns the number of bytes required for all candidate lists if successful, or 0 otherwise.




## -remarks



Applications typically call this function in response to an <a href="https://msdn.microsoft.com/439ff125-2731-4eb1-8287-4ca8ace7d8ec">IMN_OPENCANDIDATE</a> or <a href="https://msdn.microsoft.com/0a276f9c-cece-4fa6-b71a-ba0daad5ca05">IMN_CHANGECANDIDATE</a> command.




## -see-also




<a href="https://msdn.microsoft.com/0a276f9c-cece-4fa6-b71a-ba0daad5ca05">IMN_CHANGECANDIDATE</a>



<a href="https://msdn.microsoft.com/439ff125-2731-4eb1-8287-4ca8ace7d8ec">IMN_OPENCANDIDATE</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

