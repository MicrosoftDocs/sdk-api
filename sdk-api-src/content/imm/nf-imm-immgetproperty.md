---
UID: NF:imm.ImmGetProperty
title: ImmGetProperty function (imm.h)
description: The ImmGetProperty function (imm.h) retrieves the property and capabilities of the IME associated with the specified input locale.
helpviewer_keywords: ["IGP_CONVERSION","IGP_GETIMEVERSION","IGP_PROPERTY","IGP_SELECT","IGP_SENTENCE","IGP_SETCOMPSTR","IGP_UI","ImmGetProperty","ImmGetProperty function [Internationalization for Windows Applications]","_win32_ImmGetProperty","imm/ImmGetProperty","intl.immgetproperty"]
old-location: intl\immgetproperty.htm
tech.root: Intl
ms.assetid: b8552c4e-1841-4202-a71e-4b4eae99c528
ms.date: 08/04/2022
ms.keywords: IGP_CONVERSION, IGP_GETIMEVERSION, IGP_PROPERTY, IGP_SELECT, IGP_SENTENCE, IGP_SETCOMPSTR, IGP_UI, ImmGetProperty, ImmGetProperty function [Internationalization for Windows Applications], _win32_ImmGetProperty, imm/ImmGetProperty, intl.immgetproperty
req.header: imm.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ImmGetProperty
 - imm/ImmGetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-imm-l1-1-2.dll
 - Imm32.dll
 - Ext-MS-Win-imm-l1-1-0.dll
 - ext-ms-win-imm-l1-1-1.dll
api_name:
 - ImmGetProperty
---

# ImmGetProperty function


## -description

Retrieves the property and capabilities of the IME associated with the specified input locale.

## -parameters

### -param HKL [in]

Input locale identifier.

### -param DWORD [in]

Type of property information to retrieve. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IGP_CONVERSION"></a><a id="igp_conversion"></a><dl>
<dt><b>IGP_CONVERSION</b></dt>
</dl>
</td>
<td width="60%">
Conversion capabilities.

</td>
</tr>
<tr>
<td width="40%"><a id="IGP_GETIMEVERSION"></a><a id="igp_getimeversion"></a><dl>
<dt><b>IGP_GETIMEVERSION</b></dt>
</dl>
</td>
<td width="60%">
System version number for which the specified IME was created.

</td>
</tr>
<tr>
<td width="40%"><a id="IGP_PROPERTY"></a><a id="igp_property"></a><dl>
<dt><b>IGP_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
Property information.

</td>
</tr>
<tr>
<td width="40%"><a id="IGP_SELECT"></a><a id="igp_select"></a><dl>
<dt><b>IGP_SELECT</b></dt>
</dl>
</td>
<td width="60%">
Selection inheritance capabilities.

</td>
</tr>
<tr>
<td width="40%"><a id="IGP_SENTENCE"></a><a id="igp_sentence"></a><dl>
<dt><b>IGP_SENTENCE</b></dt>
</dl>
</td>
<td width="60%">
Sentence mode capabilities.

</td>
</tr>
<tr>
<td width="40%"><a id="IGP_SETCOMPSTR"></a><a id="igp_setcompstr"></a><dl>
<dt><b>IGP_SETCOMPSTR</b></dt>
</dl>
</td>
<td width="60%">
Composition string capabilities.

</td>
</tr>
<tr>
<td width="40%"><a id="IGP_UI"></a><a id="igp_ui"></a><dl>
<dt><b>IGP_UI</b></dt>
</dl>
</td>
<td width="60%">
User interface capabilities.

</td>
</tr>
</table>

## -returns

Returns the property or capability value, depending on the value of the <i>dwIndex</i> parameter. If <i>dwIndex</i> is set to IGP_PROPERTY, the function returns one or more of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>IME_PROP_AT_CARET</td>
<td>If set, conversion window is at the caret position. If clear, the window is near the caret position.</td>
</tr>
<tr>
<td>IME_PROP_SPECIAL_UI</td>
<td>If set, the IME has a nonstandard user interface. The application should not draw in the IME window.</td>
</tr>
<tr>
<td>IME_PROP_CANDLIST_START_FROM_1</td>
<td>If set, strings in the candidate list are numbered starting at 1. If clear, strings start at 0.</td>
</tr>
<tr>
<td>IME_PROP_UNICODE</td>
<td>If set, the IME is viewed as a Unicode IME. The operating system and the IME communicate through the Unicode IME interface. If clear, the IME uses the ANSI interface to communicate with the operating system.</td>
</tr>
<tr>
<td>IME_PROP_COMPLETE_ON_UNSELECT</td>
<td>If set, the IME completes the composition string when the IME is deactivated. If clear, the IME cancels the composition string when the IME is deactivated, for example, from a keyboard layout change.</td>
</tr>
<tr>
<td>IME_PROP_ACCEPT_WIDE_VKEY</td>
<td>If set, the IME processes the injected Unicode that came from the <a href="/windows/desktop/api/winuser/nf-winuser-sendinput">SendInput</a> function by using VK_PACKET. If clear, the IME might not process the injected Unicode, and might send the injected Unicode to the application directly.</td>
</tr>
</table>
 

If <i>dwIndex</i> is set to IGP_UI, the function returns one or more of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>UI_CAP_2700</td>
<td>Support text escapement values of 0 or 2700. For more information, see the <b>lfEscapement</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure.</td>
</tr>
<tr>
<td>UI_CAP_ROT90</td>
<td>Support text escapement values of 0, 900, 1800, or 2700. For more information, see <b>lfEscapement</b>.</td>
</tr>
<tr>
<td>UI_CAP_ROTANY</td>
<td>Support any text escapement value. For more information, see <b>lfEscapement</b>.</td>
</tr>
</table>
 

If <i>dwIndex</i> is set to IGP_SETCOMPSTR, the function returns one or more of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>SCS_CAP_COMPSTR</td>
<td>Create the composition string by calling the <a href="/windows/desktop/api/imm/nf-imm-immsetcompositionstringa">ImmSetCompositionString</a> function with the SCS_SETSTR value.</td>
</tr>
<tr>
<td>SCS_CAP_MAKEREAD</td>
<td>Create the reading string from corresponding composition string when using the <a href="/windows/desktop/api/imm/nf-imm-immsetcompositionstringa">ImmSetCompositionString</a> function with SCS_SETSTR and without setting <i>lpRead</i>.</td>
</tr>
<tr>
<td>SCS_CAP_SETRECONVERTSTRING:</td>
<td>This IME can support reconversion. Use <a href="/windows/desktop/api/imm/nf-imm-immsetcompositionstringa">ImmSetCompositionString</a> to do reconversion.</td>
</tr>
</table>
 

If <i>dwIndex</i> is set to IGP_SELECT, the function returns one or more of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>SELECT_CAP_CONVMODE</td>
<td>Inherit conversion mode when a new IME is selected.</td>
</tr>
<tr>
<td>SELECT_CAP_SENTENCE</td>
<td>Inherit sentence mode when a new IME is selected.</td>
</tr>
</table>
 

If <i>dwIndex</i> is set to IGP_GETIMEVERSION, the function returns one or more of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>IMEVER_0310</td>
<td>The IME was created for Windows 3.1.</td>
</tr>
<tr>
<td>IMEVER_0400</td>
<td>The IME was created for Windows Me/98/95.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imm/nf-imm-immsetcompositionstringa">ImmSetCompositionString</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
