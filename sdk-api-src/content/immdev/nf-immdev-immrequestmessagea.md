---
UID: NF:immdev.ImmRequestMessageA
title: ImmRequestMessageA function
author: windows-sdk-content
description: Generates a WM_IME_REQUEST message.
old-location: intl\immrequestmessage.htm
tech.root: Intl
ms.assetid: 70c90851-b6a4-41ce-a048-c828adcd4ed8
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ImmRequestMessage, ImmRequestMessage function [Internationalization for Windows Applications], ImmRequestMessageA, ImmRequestMessageW, immdev/ImmRequestMessage, immdev/ImmRequestMessageA, immdev/ImmRequestMessageW, intl.immrequestmessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: immdev.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmRequestMessageW (Unicode) and ImmRequestMessageA (ANSI)
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
 - ImmRequestMessage
 - ImmRequestMessageA
 - ImmRequestMessageW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmRequestMessageA function


## -description


Generates a <a href="https://msdn.microsoft.com/c5e9f256-eed2-46cb-bb33-0e640a975f1f">WM_IME_REQUEST</a> message.


## -parameters




### -param HIMC [in]

Handle to the target input context.


### -param WPARAM [in]

Value of the <i>wParam</i> parameter for the <a href="https://msdn.microsoft.com/c5e9f256-eed2-46cb-bb33-0e640a975f1f">WM_IME_REQUEST</a> message.


### -param LPARAM [in]

Value of the <i>lParam</i> parameter for the <a href="https://msdn.microsoft.com/c5e9f256-eed2-46cb-bb33-0e640a975f1f">WM_IME_REQUEST</a> message.


## -returns



Returns an operation-specific value if successful, or 0 otherwise.




## -remarks



IME must use this function instead of sending the <a href="https://msdn.microsoft.com/c5e9f256-eed2-46cb-bb33-0e640a975f1f">WM_IME_REQUEST</a> message to the application in a call to <a href="https://msdn.microsoft.com/en-us/library/ms714170(v=VS.85).aspx">SendMessage</a>.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>



<a href="https://msdn.microsoft.com/c5e9f256-eed2-46cb-bb33-0e640a975f1f">WM_IME_REQUEST</a>
 

 

