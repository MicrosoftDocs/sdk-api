---
UID: NF:immdev.ImmGetCandidateWindow
title: ImmGetCandidateWindow function (immdev.h)
description: Retrieves information about the candidates window.helpviewer_keywords: ["ImmGetCandidateWindow","ImmGetCandidateWindow function [Internationalization for Windows Applications]","_win32_ImmGetCandidateWindow","imm/ImmGetCandidateWindow","intl.immgetcandidatewindow"]
old-location: intl\immgetcandidatewindow.htm
tech.root: Intl
ms.assetid: 39800693-0eb5-4807-94b2-d11e6f98ba2c
ms.date: 12/05/2018
ms.keywords: ImmGetCandidateWindow, ImmGetCandidateWindow function [Internationalization for Windows Applications], _win32_ImmGetCandidateWindow, imm/ImmGetCandidateWindow, intl.immgetcandidatewindow
f1_keywords:
- immdev/ImmGetCandidateWindow
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
req.unicode-ansi: 
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
- Ext-MS-Win-imm-l1-1-0.dll
- ext-ms-win-imm-l1-1-1.dll
api_name:
- ImmGetCandidateWindow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/imm/ns-imm-candidateform">CANDIDATEFORM</a> structure in which this function retrieves information about the candidates window.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imm/ns-imm-candidateform">CANDIDATEFORM</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

