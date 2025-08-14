---
UID: NF:immdev.ImmDisableLegacyIME
title: ImmDisableLegacyIME function (immdev.h)
description: The ImmDisableLegacyIME function (immdev.h) indicates that this thread is a Windows Store app UI thread.
helpviewer_keywords: ["IMMDisableLegacyIME","IMMDisableLegacyIME function [Internationalization for Windows Applications]","ImmDisableLegacyIME","imm/IMMDisableLegacyIME","intl.immdisablelegacyime"]
old-location: intl\immdisablelegacyime.htm
tech.root: Intl
ms.assetid: 5B207438-B437-45B0-AE0C-DDB1B19488F2
ms.date: 08/04/2022
ms.keywords: IMMDisableLegacyIME, IMMDisableLegacyIME function [Internationalization for Windows Applications], ImmDisableLegacyIME, imm/IMMDisableLegacyIME, intl.immdisablelegacyime
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImmDisableLegacyIME
 - immdev/ImmDisableLegacyIME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-imm-l1-1-2.dll
 - ext-ms-win-imm-l1-1-1.dll
 - ext-ms-win-imm-l1-1-0.dll
 - imm32.dll
api_name:
 - IMMDisableLegacyIME
---

# ImmDisableLegacyIME function


## -description

Indicates that this thread is a Windows Store app UI thread.



## -returns

Returns <b>TRUE</b> if successful;   otherwise, <b>FALSE</b>.

## -remarks

Windows Store app brokers such as explorer.exe should call this function in Windows Store app UI threads to ensure that only IMEs that are compatible with  Windows Store apps are made available.  Those Windows Store app threads that don't require IME input should call <a href="/windows/desktop/api/imm/nf-imm-immdisableime">ImmDisableIME</a> to disable IMM entirely for that thread.

The app must call this function before the first top-level window in the thread receives the <a href="/windows/desktop/winmsg/wm-create">WM_CREATE</a> message. Thus, the app must call this function in one of the following places:

<ul>
<li>Any time before  <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> is called to create the first top-level window.</li>
<li>In the <a href="/windows/desktop/winmsg/wm-nccreate">WM_NCCREATE</a> handler for the first top-level window.</li>
</ul>

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
