---
UID: NF:imm.ImmIsIME
title: ImmIsIME function
author: windows-sdk-content
description: Determines if the specified input locale has an IME.
old-location: intl\immisime.htm
tech.root: Intl
ms.assetid: 87bd38ce-c82c-4a65-8157-fcd69bc79566
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ImmIsIME, ImmIsIME function [Internationalization for Windows Applications], _win32_ImmIsIME, imm/ImmIsIME, intl.immisime
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
 - ImmIsIME
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ImmIsIME
: 
---

# ImmIsIME function


## -description


Determines if the specified input locale has an IME.


## -parameters




### -param HKL [in]

Input locale identifier.


## -returns



Returns a nonzero value if the specified locale has an IME, or 0 otherwise.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

