---
UID: NF:wingdi.TranslateCharsetInfo
title: TranslateCharsetInfo function
author: windows-sdk-content
description: Translates character set information and sets all members of a destination structure to appropriate values.
old-location: intl\translatecharsetinfo.htm
old-project: Intl
ms.assetid: 0e6e81f1-ec7b-42ba-8706-a352349fa6ab
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: TCI_SRCCHARSET, TCI_SRCCODEPAGE, TCI_SRCFONTSIG, TCI_SRCLOCALE, TranslateCharsetInfo, TranslateCharsetInfo function [Internationalization for Windows Applications], _win32_TranslateCharsetInfo, intl.translatecharsetinfo, wingdi/TranslateCharsetInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - Ext-MS-Win-GDI-Font-l1-1-0.dll
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - TranslateCharsetInfo
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# TranslateCharsetInfo function


## -description


Translates character set information and sets all members of a destination structure to appropriate values.


## -parameters




### -param lpSrc [in, out]

Pointer to the <b>fsCsb</b> member of a <a href="https://msdn.microsoft.com/5331da53-7e3d-46e9-a922-da04fedc8382">FONTSIGNATURE</a> structure if <i>dwFlags</i> is set to TCI_SRCFONTSIG. Otherwise, this parameter is set to a DWORD value indicating the source.


### -param lpCs [out]

Pointer to a <a href="https://msdn.microsoft.com/4f815f53-9fac-41f3-9493-bd8d68cff543">CHARSETINFO</a> structure that receives the translated character set information.


### -param dwFlags [in]

Flags specifying how to perform the translation. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TCI_SRCCHARSET"></a><a id="tci_srccharset"></a><dl>
<dt><b>TCI_SRCCHARSET</b></dt>
</dl>
</td>
<td width="60%">
Source contains the character set value in the low word, and 0 in the high word.

</td>
</tr>
<tr>
<td width="40%"><a id="TCI_SRCCODEPAGE"></a><a id="tci_srccodepage"></a><dl>
<dt><b>TCI_SRCCODEPAGE</b></dt>
</dl>
</td>
<td width="60%">
Source is a code page identifier in the low word and 0 in the high word.

</td>
</tr>
<tr>
<td width="40%"><a id="TCI_SRCFONTSIG"></a><a id="tci_srcfontsig"></a><dl>
<dt><b>TCI_SRCFONTSIG</b></dt>
</dl>
</td>
<td width="60%">
Source is the code page bitfield portion of a <a href="https://msdn.microsoft.com/5331da53-7e3d-46e9-a922-da04fedc8382">FONTSIGNATURE</a> structure. On input this should have only one Windows code-page bit set, either for an ANSI code page value or for a common ANSI and OEM value (for OEM values, bits 32-63 must be clear). On output, this has only one bit set.

If the TCI_SRCFONTSIG value is given, the <i>lpSrc</i> parameter must be the address of the code-page bitfield. If any other TCI_ value is given, the <i>lpSrc</i> parameter must be a value not an address.

</td>
</tr>
<tr>
<td width="40%"><a id="TCI_SRCLOCALE"></a><a id="tci_srclocale"></a><dl>
<dt><b>TCI_SRCLOCALE</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows 2000:</b> Source is the locale identifier (LCID) or language identifier of the keyboard layout. If it is a language identifier, the value is in the low word.

</td>
</tr>
</table>
 


## -returns



Returns a nonzero value if successful, or 0 otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/4f815f53-9fac-41f3-9493-bd8d68cff543">CHARSETINFO</a>



<a href="https://msdn.microsoft.com/5331da53-7e3d-46e9-a922-da04fedc8382">FONTSIGNATURE</a>



<a href="https://msdn.microsoft.com/1799f5da-1391-4b6e-ac13-718017a77557">Unicode and Character Set Functions</a>



<a href="https://msdn.microsoft.com/8c1c6582-b58c-4008-9ce5-208acc191d9f">Unicode and Character Sets</a>
 

 

