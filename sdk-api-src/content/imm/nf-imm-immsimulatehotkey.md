---
UID: NF:imm.ImmSimulateHotKey
title: ImmSimulateHotKey function
author: windows-sdk-content
description: Simulates the specified IME hot key, causing the same response as if the user presses the hot key in the specified window.
old-location: intl\immsimulatehotkey.htm
old-project: Intl
ms.assetid: 24d5dd3c-01bd-4665-ad45-9f93edb212b3
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ImmSimulateHotKey, ImmSimulateHotKey function [Internationalization for Windows Applications], _win32_ImmSimulateHotKey, imm/ImmSimulateHotKey, intl.immsimulatehotkey
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
 - ImmSimulateHotKey
product: Windows
targetos: Windows
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# ImmSimulateHotKey function


## -description


Simulates the specified IME hot key, causing the same response as if the user presses the hot key in the specified window.


## -parameters




### -param HWND

TBD


### -param DWORD

TBD




#### - dwHotKeyID [in]

Identifier of the IME hot key. For more information, see <a href="https://msdn.microsoft.com/a262ef4e-d8ab-4eb6-88c6-023b90850cc6">IME Hot Key Identifiers</a>.


#### - hWnd [in]

Handle to the window.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

