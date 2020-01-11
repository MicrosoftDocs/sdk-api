---
UID: NF:immdev.ImmInstallIMEA
title: ImmInstallIMEA function (immdev.h)
description: Installs an IME.
old-location: intl\imminstallime.htm
tech.root: Intl
ms.assetid: 8743908b-c9b4-41ff-952e-039253fb1246
ms.date: 12/05/2018
ms.keywords: ImmInstallIME, ImmInstallIME function [Internationalization for Windows Applications], ImmInstallIMEA, ImmInstallIMEW, _win32_ImmInstallIME, imm/ImmInstallIME, imm/ImmInstallIMEA, imm/ImmInstallIMEW, intl.imminstallime
f1_keywords:
- immdev/ImmInstallIME
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
req.unicode-ansi: ImmInstallIMEW (Unicode) and ImmInstallIMEA (ANSI)
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
api_name:
- ImmInstallIME
- ImmInstallIMEA
- ImmInstallIMEW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmInstallIMEA function


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




<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

