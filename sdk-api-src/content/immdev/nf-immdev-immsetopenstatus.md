---
UID: NF:immdev.ImmSetOpenStatus
title: ImmSetOpenStatus function
author: windows-sdk-content
description: Opens or closes the IME.
old-location: intl\immsetopenstatus.htm
tech.root: Intl
ms.assetid: 4c6dfc40-56d3-41bb-8094-1f30dbb27cf5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ImmSetOpenStatus, ImmSetOpenStatus function [Internationalization for Windows Applications], _win32_ImmSetOpenStatus, imm/ImmSetOpenStatus, intl.immsetopenstatus
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
 - ImmSetOpenStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmSetOpenStatus function


## -description


Opens or closes the IME.


## -parameters




### -param HIMC [in]

Handle to the input context.


### -param BOOL [in]

<b>TRUE</b> if the IME is open, or <b>FALSE</b> if it is closed.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



This function causes an <a href="https://msdn.microsoft.com/cc6fa7f4-b85a-486a-985d-53c071321bd1">IMN_SETOPENSTATUS</a> command to be sent to the application.




## -see-also




<a href="https://msdn.microsoft.com/cc6fa7f4-b85a-486a-985d-53c071321bd1">IMN_SETOPENSTATUS</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

