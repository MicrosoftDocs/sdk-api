---
UID: NF:immdev.ImmGetCandidateWindow
title: ImmGetCandidateWindow function (immdev.h)
description: The ImmGetCandidateWindow function (immdev.h) retrieves information about the candidates window. 
helpviewer_keywords: ["ImmGetCandidateWindow","ImmGetCandidateWindow function [Internationalization for Windows Applications]","_win32_ImmGetCandidateWindow","imm/ImmGetCandidateWindow","intl.immgetcandidatewindow"]
old-location: intl\immgetcandidatewindow.htm
tech.root: Intl
ms.assetid: 39800693-0eb5-4807-94b2-d11e6f98ba2c
ms.date: 08/04/2022
ms.keywords: ImmGetCandidateWindow, ImmGetCandidateWindow function [Internationalization for Windows Applications], _win32_ImmGetCandidateWindow, imm/ImmGetCandidateWindow, intl.immgetcandidatewindow
req.header: immdev.h
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
 - ImmGetCandidateWindow
 - immdev/ImmGetCandidateWindow
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
 - ImmGetCandidateWindow
---

# ImmGetCandidateWindow function


## -description

Retrieves information about the candidates window.

## -parameters

### -param HIMC [in]

Handle to the input context.

### -param DWORD [in]

Index of the candidates window.

### -param lpCandidate [out]

Pointer to a <a href="/windows/desktop/api/imm/ns-imm-candidateform">CANDIDATEFORM</a> structure in which this function retrieves information about the candidates window.

## -returns

Returns a nonzero value if successful, or 0 otherwise.

## -see-also

<a href="/windows/desktop/api/imm/ns-imm-candidateform">CANDIDATEFORM</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
