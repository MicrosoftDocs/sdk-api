---
UID: NN:ctffunc.ITfFnGetPreferredTouchKeyboardLayout
title: ITfFnGetPreferredTouchKeyboardLayout (ctffunc.h)
description: The ITfFnGetPreferredTouchKeyboardLayout interface is implemented by a text service to specify the use of a particular keyboard layout supported by the inbox Windows 8 touch keyboard.
helpviewer_keywords: ["ITfFnGetPreferredTouchKeyboardLayout","ITfFnGetPreferredTouchKeyboardLayout interface [Text Services Framework]","ITfFnGetPreferredTouchKeyboardLayout interface [Text Services Framework]","described","ctffunc/ITfFnGetPreferredTouchKeyboardLayout","tsf.itffngetpreferredtouchkeyboardlayout"]
old-location: tsf\itffngetpreferredtouchkeyboardlayout.htm
tech.root: TSF
ms.assetid: 1BC4A446-AEDC-44AA-9BD7-786917AD2556
ms.date: 12/05/2018
ms.keywords: ITfFnGetPreferredTouchKeyboardLayout, ITfFnGetPreferredTouchKeyboardLayout interface [Text Services Framework], ITfFnGetPreferredTouchKeyboardLayout interface [Text Services Framework],described, ctffunc/ITfFnGetPreferredTouchKeyboardLayout, tsf.itffngetpreferredtouchkeyboardlayout
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfFnGetPreferredTouchKeyboardLayout
 - ctffunc/ITfFnGetPreferredTouchKeyboardLayout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ctffunc.h
api_name:
 - ITfFnGetPreferredTouchKeyboardLayout
---

# ITfFnGetPreferredTouchKeyboardLayout interface


## -description

The <b>ITfFnGetPreferredTouchKeyboardLayout</b> interface is implemented by a text service to specify the use of a particular keyboard layout supported by the inbox Windows 8 touch keyboard.

When an IME is active the touch keyboard will use <a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> with <b>IID_ITfFnGetPreferredTouchKeyboardLayout</b> to query the IME for this function.

If the function is not supported by the IME, then the touch keyboard will show the default layout for the language.

## -inheritance

The <b>ITfFnGetPreferredTouchKeyboardLayout</b> interface inherits from <a href="/windows/desktop/api/msctf/nn-msctf-itffunction">ITfFunction</a>. <b>ITfFnGetPreferredTouchKeyboardLayout</b> also has these types of members:

## -remarks

For more information on the layouts which can be specified, see GetLayout.

This interface applies only to IMEs written using the Text Services Framework and not to legacy IMM32 IMEs, and it only applies to the following input languages:

<ul>
<li>Japanese</li>
<li>Korean</li>
<li>Simplified Chinese</li>
<li>Traditional Chinese</li>
</ul>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itffunction">ITfFunction</a>
