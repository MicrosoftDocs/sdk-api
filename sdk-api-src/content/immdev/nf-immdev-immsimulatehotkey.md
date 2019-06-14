---
UID: NF:immdev.ImmSimulateHotKey
title: ImmSimulateHotKey function (immdev.h)
author: windows-sdk-content
description: Simulates the specified IME hot key, causing the same response as if the user presses the hot key in the specified window.
old-location: intl\immsimulatehotkey.htm
tech.root: Intl
ms.assetid: 24d5dd3c-01bd-4665-ad45-9f93edb212b3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ImmSimulateHotKey, ImmSimulateHotKey function [Internationalization for Windows Applications], _win32_ImmSimulateHotKey, imm/ImmSimulateHotKey, intl.immsimulatehotkey
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
api_name:
 - ImmSimulateHotKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmSimulateHotKey function


## -description


Simulates the specified IME hot key, causing the same response as if the user presses the hot key in the specified window.


## -parameters




### -param HWND [in]

Handle to the window.


### -param DWORD [in]

Identifier of the IME hot key. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Intl/ime-hot-key-identifiers">IME Hot Key Identifiers</a>.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

