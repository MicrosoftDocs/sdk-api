---
UID: NF:immdev.ImmGetCandidateListCountW
title: ImmGetCandidateListCountW function (immdev.h)
description: Retrieves the size of the candidate lists.
old-location: intl\immgetcandidatelistcount.htm
tech.root: Intl
ms.assetid: da7c4eee-3c79-4ea8-b9a5-3b43befa0021
ms.date: 12/05/2018
ms.keywords: ImmGetCandidateListCount, ImmGetCandidateListCount function [Internationalization for Windows Applications], ImmGetCandidateListCountA, ImmGetCandidateListCountW, _win32_ImmGetCandidateListCount, imm/ImmGetCandidateListCount, imm/ImmGetCandidateListCountA, imm/ImmGetCandidateListCountW, intl.immgetcandidatelistcount
f1_keywords:
- immdev/ImmGetCandidateListCount
dev_langs:
- c++
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmGetCandidateListCountW function


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



Applications typically call this function in response to an <a href="https://docs.microsoft.com/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a> or <a href="https://docs.microsoft.com/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a> command.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

