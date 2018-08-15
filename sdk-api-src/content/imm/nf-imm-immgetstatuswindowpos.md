---
UID: NF:imm.ImmGetStatusWindowPos
title: ImmGetStatusWindowPos function
author: windows-sdk-content
description: Retrieves the position of the status window.
old-location: intl\immgetstatuswindowpos.htm
old-project: Intl
ms.assetid: 785d8523-14a7-4443-8326-34ca197b1cff
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ImmGetStatusWindowPos, ImmGetStatusWindowPos function [Internationalization for Windows Applications], _win32_ImmGetStatusWindowPos, imm/ImmGetStatusWindowPos, intl.immgetstatuswindowpos
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: imm.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: IMECOMPOSITIONSTRINGINFO, *LPIMECOMPOSITIONSTRINGINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imm32.dll
api_name:
 - ImmGetStatusWindowPos
product: Windows
targetos: Windows
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# ImmGetStatusWindowPos function


## -description


Retrieves the position of the status window.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param lpptPos [out]

Pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure in which the function retrieves the position coordinates. These are screen coordinates, relative to the upper left corner of the screen.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

