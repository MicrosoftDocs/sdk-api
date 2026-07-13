---
UID: NF:imm.ImmSetCandidateWindow
title: ImmSetCandidateWindow function (imm.h)
description: The ImmSetCandidateWindow function (imm.h) sets information about the candidates window.
helpviewer_keywords: ["ImmSetCandidateWindow","ImmSetCandidateWindow function [Internationalization for Windows Applications]","_win32_ImmSetCandidateWindow","imm/ImmSetCandidateWindow","intl.immsetcandidatewindow"]
old-location: intl\immsetcandidatewindow.htm
tech.root: Intl
ms.assetid: 4b82a5a3-1e31-4d50-9a0f-890e94d12201
ms.date: 08/04/2022
ms.keywords: ImmSetCandidateWindow, ImmSetCandidateWindow function [Internationalization for Windows Applications], _win32_ImmSetCandidateWindow, imm/ImmSetCandidateWindow, intl.immsetcandidatewindow
req.header: imm.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - ImmSetCandidateWindow
 - imm/ImmSetCandidateWindow
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
 - Ext-MS-Win-imm-l1-1-0.dll
 - ext-ms-win-imm-l1-1-1.dll
api_name:
 - ImmSetCandidateWindow
---

# ImmSetCandidateWindow function


## -description

Sets information about the candidates window.

## -parameters

### -param HIMC [in]

Handle to the input context.

### -param lpCandidate [in]

Pointer to a <a href="/windows/desktop/api/imm/ns-imm-candidateform">CANDIDATEFORM</a> structure that contains information about the candidates window.

## -returns

Returns a nonzero value if successful, or 0 otherwise.

## -remarks

This function causes an <a href="/windows/desktop/Intl/imn-setcandidatepos">IMN_SETCANDIDATEPOS</a> command to be sent. Both the IME and the application call this function.

## -see-also

<a href="/windows/desktop/api/imm/ns-imm-candidateform">CANDIDATEFORM</a>



<a href="/windows/desktop/Intl/imn-setcandidatepos">IMN_SETCANDIDATEPOS</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
