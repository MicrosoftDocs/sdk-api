---
UID: NF:imm.ImmInstallIMEW
title: ImmInstallIMEW function
author: windows-sdk-content
description: Installs an IME.
old-location: intl\imminstallime.htm
old-project: Intl
ms.assetid: 8743908b-c9b4-41ff-952e-039253fb1246
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ImmInstallIME, ImmInstallIME function [Internationalization for Windows Applications], ImmInstallIMEA, ImmInstallIMEW, _win32_ImmInstallIME, imm/ImmInstallIME, imm/ImmInstallIMEA, imm/ImmInstallIMEW, intl.imminstallime
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
req.unicode-ansi: ImmInstallIMEW (Unicode) and ImmInstallIMEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMECOMPOSITIONSTRINGINFO, *LPIMECOMPOSITIONSTRINGINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Imm32.dll
api_name:
-	ImmInstallIME
-	ImmInstallIMEA
-	ImmInstallIMEW
product: Windows
targetos: Windows
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# ImmInstallIMEW function


## -description


Installs an IME.


## -parameters




### -param lpszIMEFileName [in]

Pointer to a null-terminated string that specifies the full path of the IME.


### -param lpszLayoutText [in]

Pointer to a null-terminated string that specifies the name of the IME and the associated layout text.


## -returns



Returns the input locale identifier for the IME.




## -remarks



This function is intended to be used by IME setup applications only.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

