---
UID: NF:imm.ImmConfigureIMEA
title: ImmConfigureIMEA function
author: windows-sdk-content
description: Displays the configuration dialog box for the IME of the specified input locale identifier.
old-location: intl\immconfigureime.htm
old-project: Intl
ms.assetid: acefb3a0-82c7-4af6-8ef0-aba561f570c1
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IME_CONFIG_GENERAL, IME_CONFIG_REGISTERWORD, IME_CONFIG_SELECTDICTIONARY, ImmConfigureIME, ImmConfigureIME function [Internationalization for Windows Applications], ImmConfigureIMEA, ImmConfigureIMEW, _win32_ImmConfigureIME, imm/ImmConfigureIME, imm/ImmConfigureIMEA, imm/ImmConfigureIMEW, intl.immconfigureime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmConfigureIMEW (Unicode) and ImmConfigureIMEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMECOMPOSITIONSTRINGINFO, *LPIMECOMPOSITIONSTRINGINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	imm32.dll
api_name:
-	ImmConfigureIME
-	ImmConfigureIMEA
-	ImmConfigureIMEW
product: Windows
targetos: Windows
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# ImmConfigureIMEA function


## -description


Displays the configuration dialog box for the IME of the specified input locale identifier.


## -parameters




### -param HKL

TBD


### -param HWND

TBD


### -param DWORD

TBD


### -param LPVOID

TBD




#### - dwMode [in]

Flags specifying the type of dialog box to display. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IME_CONFIG_GENERAL"></a><a id="ime_config_general"></a><dl>
<dt><b>IME_CONFIG_GENERAL</b></dt>
</dl>
</td>
<td width="60%">
Display general-purpose configuration dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="IME_CONFIG_REGISTERWORD"></a><a id="ime_config_registerword"></a><dl>
<dt><b>IME_CONFIG_REGISTERWORD</b></dt>
</dl>
</td>
<td width="60%">
Display register word dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="IME_CONFIG_SELECTDICTIONARY"></a><a id="ime_config_selectdictionary"></a><dl>
<dt><b>IME_CONFIG_SELECTDICTIONARY</b></dt>
</dl>
</td>
<td width="60%">
Display dictionary selection dialog box.

</td>
</tr>
</table>
 


#### - hKL [in]

Input locale identifier of an IME.


#### - hWnd [in]

Handle to the parent window for the dialog box.


#### - lpData [in]

Pointer to supplemental data. If <i>dwMode</i> is set to IME_CONFIG_REGISTERWORD, this parameter must indicate a <a href="https://msdn.microsoft.com/70a11a96-a0e3-4741-be91-b85eb38cd767">REGISTERWORD</a> structure. If <i>dwMode</i> is not IME_CONFIG_REGISTERWORD, this parameter is ignored.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>



<a href="https://msdn.microsoft.com/70a11a96-a0e3-4741-be91-b85eb38cd767">REGISTERWORD</a>
 

 

