---
UID: NF:immdev.ImmGetCandidateListCountW
title: ImmGetCandidateListCountW function (immdev.h)
description: The ImmGetCandidateListCountW (Unicode) function (immdev.h) retrieves the size of the candidate lists.
helpviewer_keywords: ["ImmGetCandidateListCount", "ImmGetCandidateListCount function [Internationalization for Windows Applications]", "ImmGetCandidateListCountW", "_win32_ImmGetCandidateListCount", "intl.immgetcandidatelistcount"]
old-location: intl\immgetcandidatelistcount.htm
tech.root: Intl
ms.assetid: da7c4eee-3c79-4ea8-b9a5-3b43befa0021
ms.date: 08/04/2022
ms.keywords: ImmGetCandidateListCount, ImmGetCandidateListCount function [Internationalization for Windows Applications], ImmGetCandidateListCountA, ImmGetCandidateListCountW, _win32_ImmGetCandidateListCount, imm/ImmGetCandidateListCount, imm/ImmGetCandidateListCountA, imm/ImmGetCandidateListCountW, intl.immgetcandidatelistcount
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImmGetCandidateListCountW
 - immdev/ImmGetCandidateListCountW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-imm-l1-1-2.dll
 - Imm32.dll
api_name:
 - ImmGetCandidateListCount
 - ImmGetCandidateListCountA
 - ImmGetCandidateListCountW
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

Applications typically call this function in response to an <a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a> or <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a> command.





> [!NOTE]
> The immdev.h header defines ImmGetCandidateListCount as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a>



<a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
