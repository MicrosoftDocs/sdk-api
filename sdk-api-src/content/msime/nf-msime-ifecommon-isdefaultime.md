---
UID: NF:msime.IFECommon.IsDefaultIME
title: IFECommon::IsDefaultIME (msime.h)
description: Determines if the IME specified by the class ID is the default IME on a local computer.
helpviewer_keywords: ["IFECommon interface [Internationalization for Windows Applications]","IsDefaultIME method","IFECommon.IsDefaultIME","IFECommon::IsDefaultIME","IsDefaultIME","IsDefaultIME method [Internationalization for Windows Applications]","IsDefaultIME method [Internationalization for Windows Applications]","IFECommon interface","intl.ifecommon_isdefaultime","msime/IFECommon::IsDefaultIME"]
old-location: intl\ifecommon_isdefaultime.htm
tech.root: Intl
ms.assetid: FFC3E200-54D4-4C47-A4A3-87AA2A4A2232
ms.date: 12/05/2018
ms.keywords: IFECommon interface [Internationalization for Windows Applications],IsDefaultIME method, IFECommon.IsDefaultIME, IFECommon::IsDefaultIME, IsDefaultIME, IsDefaultIME method [Internationalization for Windows Applications], IsDefaultIME method [Internationalization for Windows Applications],IFECommon interface, intl.ifecommon_isdefaultime, msime/IFECommon::IsDefaultIME
req.header: msime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IFECommon::IsDefaultIME
 - msime/IFECommon::IsDefaultIME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msime.h
api_name:
 - IFECommon.IsDefaultIME
---

# IFECommon::IsDefaultIME


## -description

Determines if the IME specified by the class ID is the default IME on a local computer.

The name of the IME is obtained from the  <a href="/windows/desktop/inputdev/keyboard-input-functions">Win32 keyboard layout API</a>.

## -parameters

### -param szName [out]

The name of the IME for the specified class ID. Can be <b>NULL</b>.

### -param cszName [in]

The size of <i>szName</i> in bytes.

## -returns

<ul>
<li><b>S_OK</b> if this Microsoft IME is already the default IME.</li>
<li><b>S_FALSE</b> if this Microsoft IME is not the default IME.</li>
<li>Otherwise <b>E_FAIL</b>.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/msime/nn-msime-ifecommon">IFECommon</a>



<a href="/windows/desktop/inputdev/keyboard-input-functions">Win32 keyboard layout API</a>