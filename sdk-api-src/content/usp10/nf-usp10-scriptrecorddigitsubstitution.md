---
UID: NF:usp10.ScriptRecordDigitSubstitution
title: ScriptRecordDigitSubstitution function
author: windows-sdk-content
description: Reads the National Language Support (NLS) native digit and digit substitution settings and records them in a SCRIPT_DIGITSUBSTITUTE structure. For more information, see Digit Shapes.
old-location: intl\scriptrecorddigitsubstitution.htm
tech.root: Intl
ms.assetid: 2c8c33d5-5cd6-4734-bf44-af7d4b578672
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ScriptRecordDigitSubstitution, ScriptRecordDigitSubstitution function [Internationalization for Windows Applications], _win32_ScriptRecordDigitSubstitution, intl.scriptrecorddigitsubstitution, usp10/ScriptRecordDigitSubstitution
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - usp10.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptRecordDigitSubstitution
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ScriptRecordDigitSubstitution function


## -description


Reads the National Language Support (NLS) native digit and digit substitution settings and records them in a <a href="https://msdn.microsoft.com/e96bf8b4-7456-4e16-a623-48320104dd66">SCRIPT_DIGITSUBSTITUTE</a> structure. For more information, see <a href="https://msdn.microsoft.com/6b5267d8-b102-410c-bdc9-831555ca2f84">Digit Shapes</a>.


## -parameters




### -param Locale [in]


<a href="https://msdn.microsoft.com/ea45b0e5-7df7-47fb-8dad-fccfbe53fec0">Locale identifier</a> of the locale to query. Typically, the application should set this parameter to <a href="https://msdn.microsoft.com/9ccb489b-24d0-42e5-a01a-2cdb7c3267eb">LOCALE_USER_DEFAULT</a>. Alternatively, the setting can indicate a specific locale combined with <a href="https://msdn.microsoft.com/ab68d16b-5e1e-4af3-b048-43975cded00a">LOCALE_NOUSEROVERRIDE</a> to obtain the default settings.


### -param psds [out]

Pointer to a <a href="https://msdn.microsoft.com/e96bf8b4-7456-4e16-a623-48320104dd66">SCRIPT_DIGITSUBSTITUTE</a> structure. This structure can be passed later to <a href="https://msdn.microsoft.com/486b8a56-eb14-48c3-b2f0-f5494f79baea">ScriptApplyDigitSubstitution</a>.


## -returns



Returns S_OK if successful. The function returns a nonzero HRESULT value if it does not succeed.

Error returns include:    
<ul>
<li>E_INVALIDARG. The <i>Locale</i> parameter indicates a locale that is invalid or not installed.</li>
<li>E_POINTER. The <i>psds</i> parameter is set to <b>NULL</b>.</li>
</ul>





## -remarks



See <a href="https://msdn.microsoft.com/e1adc567-0445-4deb-8634-25653f82127c">Displaying Text with Uniscribe</a> for a discussion of the context in which this function is normally called.

This function supports context digit substitution only for Arabic and Persian locales. For other locales, context digit substitution is mapped to no substitution.

The following example shows the typical way to call this function.


```cpp
SCRIPT_DIGITSUBSTITUTE sds;
ScriptRecordDigitSubstitution(LOCALE_USER_DEFAULT, &sds);

```


At every itemization, the application can use the results as shown in the next example.


```cpp
SCRIPT_CONTROL sc = {0};
SCRIPT_STATE   ss = {0};
ScriptApplyDigitSubstitution(&sds, &sc, &ss);

```


For performance reasons, your application should not call <b>ScriptRecordDigitSubstitution</b> frequently. The function requires considerable overhead to call it every time <a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a> or <a href="https://msdn.microsoft.com/6d0e7070-159e-436b-85b5-cabb3da83f5e">ScriptStringAnalyse</a> is called. Instead, the application can save the <a href="https://msdn.microsoft.com/e96bf8b4-7456-4e16-a623-48320104dd66">SCRIPT_DIGITSUBSTITUTE</a> structure and update it only when a <a href="_win32_wm_settingchange_cpp">WM_SETTINGCHANGE</a> message is received. Alternatively, the application can update the structure when a <a href="https://msdn.microsoft.com/aad72ed5-1123-4a8b-9fc4-b54a713b635e">RegNotifyChangeKeyValue</a> call in a dedicated thread indicates a change in the registry under HKCU\Control Panel\International.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e1adc567-0445-4deb-8634-25653f82127c">Displaying Text with Uniscribe</a>



<a href="https://msdn.microsoft.com/e96bf8b4-7456-4e16-a623-48320104dd66">SCRIPT_DIGITSUBSTITUTE</a>



<a href="https://msdn.microsoft.com/486b8a56-eb14-48c3-b2f0-f5494f79baea">ScriptApplyDigitSubstitution</a>



<a href="https://msdn.microsoft.com/1491d9c5-e86b-45cc-bb47-85c8619eab69">ScriptItemize</a>



<a href="https://msdn.microsoft.com/6d0e7070-159e-436b-85b5-cabb3da83f5e">ScriptStringAnalyse</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

