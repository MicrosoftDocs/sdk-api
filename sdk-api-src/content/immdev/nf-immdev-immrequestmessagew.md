---
UID: NF:immdev.ImmRequestMessageW
title: ImmRequestMessageW function (immdev.h)

description: Generates a WM_IME_REQUEST message.
old-location: intl\immrequestmessage.htm
tech.root: Intl
ms.assetid: 70c90851-b6a4-41ce-a048-c828adcd4ed8

ms.date: 12/05/2018
ms.keywords: ImmRequestMessage, ImmRequestMessage function [Internationalization for Windows Applications], ImmRequestMessageA, ImmRequestMessageW, immdev/ImmRequestMessage, immdev/ImmRequestMessageA, immdev/ImmRequestMessageW, intl.immrequestmessage
ms.topic: function
f1_keywords: 
 - "immdev/ImmRequestMessage"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmRequestMessageW function


## -description


Generates a <a href="https://docs.microsoft.com/windows/desktop/Intl/wm-ime-request">WM_IME_REQUEST</a> message.


## -parameters




### -param HIMC [in]

Handle to the target input context.


### -param WPARAM [in]

Value of the <i>wParam</i> parameter for the <a href="https://docs.microsoft.com/windows/desktop/Intl/wm-ime-request">WM_IME_REQUEST</a> message.


### -param LPARAM [in]

Value of the <i>lParam</i> parameter for the <a href="https://docs.microsoft.com/windows/desktop/Intl/wm-ime-request">WM_IME_REQUEST</a> message.


## -returns



Returns an operation-specific value if successful, or 0 otherwise.




## -remarks



IME must use this function instead of sending the <a href="https://docs.microsoft.com/windows/desktop/Intl/wm-ime-request">WM_IME_REQUEST</a> message to the application in a call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/oe/oe-ihttpmailtransport-sendmessage">SendMessage</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/wm-ime-request">WM_IME_REQUEST</a>
 

 

