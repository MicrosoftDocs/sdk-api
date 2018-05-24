---
UID: NF:imm.ImmSetCandidateWindow
title: ImmSetCandidateWindow function
author: windows-driver-content
description: Sets information about the candidates window.
old-location: intl\immsetcandidatewindow.htm
old-project: Intl
ms.assetid: 4b82a5a3-1e31-4d50-9a0f-890e94d12201
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: ImmSetCandidateWindow, ImmSetCandidateWindow function [Internationalization for Windows Applications], _win32_ImmSetCandidateWindow, imm/ImmSetCandidateWindow, intl.immsetcandidatewindow
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IMECOMPOSITIONSTRINGINFO, *LPIMECOMPOSITIONSTRINGINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Imm32.dll
-	Ext-MS-Win-imm-l1-1-0.dll
-	ext-ms-win-imm-l1-1-1.dll
api_name:
-	ImmSetCandidateWindow
product: Windows
targetos: Windows
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# ImmSetCandidateWindow function


## -description


Sets information about the candidates window.


## -parameters




### -param HIMC

TBD


### -param lpCandidate [in]

Pointer to a <a href="https://msdn.microsoft.com/86edcfe0-07f7-4bd7-9444-3a884aeb7926">CANDIDATEFORM</a> structure that contains information about the candidates window.


#### - hIMC [in]

Handle to the input context.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



This function causes an <a href="https://msdn.microsoft.com/64252d88-130b-44c3-854a-78b01def7a13">IMN_SETCANDIDATEPOS</a> command to be sent. Both the IME and the application call this function.




## -see-also




<a href="https://msdn.microsoft.com/86edcfe0-07f7-4bd7-9444-3a884aeb7926">CANDIDATEFORM</a>



<a href="https://msdn.microsoft.com/64252d88-130b-44c3-854a-78b01def7a13">IMN_SETCANDIDATEPOS</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

