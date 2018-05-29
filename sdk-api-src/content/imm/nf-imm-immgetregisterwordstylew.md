---
UID: NF:imm.ImmGetRegisterWordStyleW
title: ImmGetRegisterWordStyleW function
author: windows-sdk-content
description: Retrieves a list of the styles supported by the IME associated with the specified input locale.
old-location: intl\immgetregisterwordstyle.htm
old-project: Intl
ms.assetid: 29ddf963-f421-4fad-9861-a6ed51e481ac
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ImmGetRegisterWordStyle, ImmGetRegisterWordStyle function [Internationalization for Windows Applications], ImmGetRegisterWordStyleA, ImmGetRegisterWordStyleW, _win32_ImmGetRegisterWordStyle, imm/ImmGetRegisterWordStyle, imm/ImmGetRegisterWordStyleA, imm/ImmGetRegisterWordStyleW, intl.immgetregisterwordstyle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmGetRegisterWordStyleW (Unicode) and ImmGetRegisterWordStyleA (ANSI)
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
api_name:
-	ImmGetRegisterWordStyle
-	ImmGetRegisterWordStyleA
-	ImmGetRegisterWordStyleW
product: Windows
targetos: Windows
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# ImmGetRegisterWordStyleW function


## -description


Retrieves a list of the styles supported by the IME associated with the specified input locale.


## -parameters




### -param HKL

TBD


### -param nItem [in]

Maximum number of styles that the output buffer can hold. The application sets this parameter to 0 if the function is to count the number of styles available in the IME.


### -param lpStyleBuf [out]

Pointer to a <a href="https://msdn.microsoft.com/72681071-58c4-490a-83d5-5013871ca875">STYLEBUF</a> structure in which the function retrieves the style information.


#### - hKL [in]

Input locale identifier.


## -returns



Returns the number of styles copied to the buffer. If the application sets the <i>nItem</i> parameter to 0, the return value is the number of styles available in the IME.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>



<a href="https://msdn.microsoft.com/72681071-58c4-490a-83d5-5013871ca875">STYLEBUF</a>
 

 

