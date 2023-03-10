---
UID: NF:usp10.ScriptGetProperties
title: ScriptGetProperties function (usp10.h)
description: Retrieves information about the current scripts.
helpviewer_keywords: ["ScriptGetProperties","ScriptGetProperties function [Internationalization for Windows Applications]","_win32_ScriptGetProperties","intl.scriptgetproperties","usp10/ScriptGetProperties"]
old-location: intl\scriptgetproperties.htm
tech.root: Intl
ms.assetid: 4799829d-8122-4bb4-839c-92f177cfd2da
ms.date: 12/05/2018
ms.keywords: ScriptGetProperties, ScriptGetProperties function [Internationalization for Windows Applications], _win32_ScriptGetProperties, intl.scriptgetproperties, usp10/ScriptGetProperties
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 5 or later on Windows Me/98/95
ms.custom: 19H1
f1_keywords:
 - ScriptGetProperties
 - usp10/ScriptGetProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - usp10.dll
 - Ext-MS-Win-usp10-l1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptGetProperties
---

# ScriptGetProperties function


## -description

Retrieves information about the current scripts.

## -parameters

### -param ppSp [out]

Pointer to an array of pointers to <a href="/windows/desktop/api/usp10/ns-usp10-script_properties">SCRIPT_PROPERTIES</a> structures indexed by script.

### -param piNumScripts [out]

Pointer to the number of scripts. The valid range for this value is 0 through <i>piNumScripts</i>-1.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

## -remarks

See <a href="/windows/desktop/Intl/determining-if-a-script-requires-glyph-shaping">Determining If a Script Requires Glyph Shaping</a> for an example of the use of this function.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/usp10/ns-usp10-script_properties">SCRIPT_PROPERTIES</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>