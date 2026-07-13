---
UID: NF:immdev.ImmRequestMessageW
title: ImmRequestMessageW function (immdev.h)
description: Generates a WM_IME_REQUEST message. (Unicode)
helpviewer_keywords: ["ImmRequestMessage", "ImmRequestMessage function [Internationalization for Windows Applications]", "ImmRequestMessageW", "immdev/ImmRequestMessage", "immdev/ImmRequestMessageW", "intl.immrequestmessage"]
old-location: intl\immrequestmessage.htm
tech.root: Intl
ms.assetid: 70c90851-b6a4-41ce-a048-c828adcd4ed8
ms.date: 12/05/2018
ms.keywords: ImmRequestMessage, ImmRequestMessage function [Internationalization for Windows Applications], ImmRequestMessageA, ImmRequestMessageW, immdev/ImmRequestMessage, immdev/ImmRequestMessageA, immdev/ImmRequestMessageW, intl.immrequestmessage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImmRequestMessageW
 - immdev/ImmRequestMessageW
dev_langs:
 - c++
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
---

# ImmRequestMessageW function


## -description

Generates a <a href="/windows/desktop/Intl/wm-ime-request">WM_IME_REQUEST</a> message.

## -parameters

### -param HIMC [in]

Handle to the target input context.

### -param WPARAM [in]

Value of the <i>wParam</i> parameter for the <a href="/windows/desktop/Intl/wm-ime-request">WM_IME_REQUEST</a> message.

### -param LPARAM [in]

Value of the <i>lParam</i> parameter for the <a href="/windows/desktop/Intl/wm-ime-request">WM_IME_REQUEST</a> message.

## -returns

Returns an operation-specific value if successful, or 0 otherwise.

## -remarks

IME must use this function instead of sending the <a href="/windows/desktop/Intl/wm-ime-request">WM_IME_REQUEST</a> message to the application in a call to <a href="/previous-versions/windows/desktop/oe/oe-ihttpmailtransport-sendmessage">SendMessage</a>.





> [!NOTE]
> The immdev.h header defines ImmRequestMessage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>



<a href="/windows/desktop/Intl/wm-ime-request">WM_IME_REQUEST</a>
