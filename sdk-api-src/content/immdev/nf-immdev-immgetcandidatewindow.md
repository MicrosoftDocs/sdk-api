---
UID: NF:immdev.ImmGetCandidateWindow
title: ImmGetCandidateWindow function
author: windows-sdk-content
description: Retrieves information about the candidates window.
old-location: intl\immgetcandidatewindow.htm
tech.root: Intl
ms.assetid: 39800693-0eb5-4807-94b2-d11e6f98ba2c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ImmGetCandidateWindow, ImmGetCandidateWindow function [Internationalization for Windows Applications], _win32_ImmGetCandidateWindow, imm/ImmGetCandidateWindow, intl.immgetcandidatewindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Pointer to a <a href="https://msdn.microsoft.com/86edcfe0-07f7-4bd7-9444-3a884aeb7926">CANDIDATEFORM</a> structure in which this function retrieves information about the candidates window.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -see-also




<a href="https://msdn.microsoft.com/86edcfe0-07f7-4bd7-9444-3a884aeb7926">CANDIDATEFORM</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

