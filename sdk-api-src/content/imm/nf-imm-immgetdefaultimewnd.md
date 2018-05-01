---
UID: NF:imm.ImmGetDefaultIMEWnd
title: ImmGetDefaultIMEWnd function
author: windows-driver-content
description: Retrieves the default window handle to the IME class.
old-location: intl\immgetdefaultimewnd.htm
old-project: Intl
ms.assetid: fc3cdfc2-fcdc-4682-b391-83ea4bb1571f
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: ImmGetDefaultIMEWnd, ImmGetDefaultIMEWnd function [Internationalization for Windows Applications], _win32_ImmGetDefaultIMEWnd, imm/ImmGetDefaultIMEWnd, intl.immgetdefaultimewnd
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
-	ImmGetDefaultIMEWnd
product: Windows
targetos: Windows
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# ImmGetDefaultIMEWnd function


## -description


Retrieves the default window handle to the IME class.


## -parameters




### -param HWND

TBD




#### - hWnd [in]

Handle to the window.


## -returns



Returns the default window handle to the IME class if successful, or <b>NULL</b> otherwise.




## -remarks



The operating system creates a default IME window for every thread. The window is created based on the IME class. The application can send the <a href="https://msdn.microsoft.com/5d3b7f8a-57c9-41e3-8022-9a3f515fc32e">WM_IME_CONTROL</a> message to this window.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>



<a href="https://msdn.microsoft.com/5d3b7f8a-57c9-41e3-8022-9a3f515fc32e">WM_IME_CONTROL</a>
 

 

