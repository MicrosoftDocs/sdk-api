---
UID: NF:immdev.ImmNotifyIME
title: ImmNotifyIME function (immdev.h)
description: The ImmNotifyIME function (immdev.h) notifies the IME about changes to the status of the input context. 
helpviewer_keywords: ["CPS_CANCEL","CPS_COMPLETE","CPS_CONVERT","CPS_REVERT","ImmNotifyIME","ImmNotifyIME function [Internationalization for Windows Applications]","NI_CHANGECANDIDATELIST","NI_CLOSECANDIDATE","NI_COMPOSITIONSTR","NI_IMEMENUSELECTED","NI_OPENCANDIDATE","NI_SELECTCANDIDATESTR","NI_SETCANDIDATE_PAGESIZE","NI_SETCANDIDATE_PAGESTART","_win32_ImmNotifyIME","imm/ImmNotifyIME","intl.immnotifyime"]
old-location: intl\immnotifyime.htm
tech.root: Intl
ms.assetid: 3ac1a32d-89a2-45e4-9dcb-b2aea5195489
ms.date: 08/04/2022
ms.keywords: CPS_CANCEL, CPS_COMPLETE, CPS_CONVERT, CPS_REVERT, ImmNotifyIME, ImmNotifyIME function [Internationalization for Windows Applications], NI_CHANGECANDIDATELIST, NI_CLOSECANDIDATE, NI_COMPOSITIONSTR, NI_IMEMENUSELECTED, NI_OPENCANDIDATE, NI_SELECTCANDIDATESTR, NI_SETCANDIDATE_PAGESIZE, NI_SETCANDIDATE_PAGESTART, _win32_ImmNotifyIME, imm/ImmNotifyIME, intl.immnotifyime
req.header: immdev.h
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
 - ImmNotifyIME
 - immdev/ImmNotifyIME
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
 - ImmNotifyIME
---

# ImmNotifyIME function


## -description

Notifies the IME about changes to the status of the input context.

## -parameters

### -param HIMC [in]

Handle to the input context.

### -param dwAction [in]

Notification code. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NI_CHANGECANDIDATELIST"></a><a id="ni_changecandidatelist"></a><dl>
<dt><b>NI_CHANGECANDIDATELIST</b></dt>
</dl>
</td>
<td width="60%">
An application changed the current selected candidate. The <i>dwIndex</i> parameter specifies an index of a candidate list to be selected and <i>dwValue</i> is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="NI_CLOSECANDIDATE"></a><a id="ni_closecandidate"></a><dl>
<dt><b>NI_CLOSECANDIDATE</b></dt>
</dl>
</td>
<td width="60%">
An application directs the IME to close a candidate list. The <i>dwIndex</i> parameter specifies an index of the list to close, and <i>dwValue</i> is not used. The IME sends a <a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a> command to the application if it closes the list.

</td>
</tr>
<tr>
<td width="40%"><a id="NI_COMPOSITIONSTR"></a><a id="ni_compositionstr"></a><dl>
<dt><b>NI_COMPOSITIONSTR</b></dt>
</dl>
</td>
<td width="60%">
An application directs the IME to carry out an action on the composition string. The <i>dwIndex</i> parameter can be CPS_CANCEL, CPS_COMPLETE, CPS_CONVERT, or CPS_REVERT.

</td>
</tr>
<tr>
<td width="40%"><a id="NI_IMEMENUSELECTED"></a><a id="ni_imemenuselected"></a><dl>
<dt><b>NI_IMEMENUSELECTED</b></dt>
</dl>
</td>
<td width="60%">
An application directs the IME to allow the application to handle the specified menu. The <i>dwIndex</i> parameter specifies the ID of the menu and <i>dwValue</i> is an application-defined value for that menu item.

</td>
</tr>
<tr>
<td width="40%"><a id="NI_OPENCANDIDATE"></a><a id="ni_opencandidate"></a><dl>
<dt><b>NI_OPENCANDIDATE</b></dt>
</dl>
</td>
<td width="60%">
An application directs the IME to open a candidate list. The <i>dwIndex</i> parameter specifies the index of the list to open, and <i>dwValue</i> is not used. The IME sends a <a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a> command to the application if it opens the list.

</td>
</tr>
<tr>
<td width="40%"><a id="NI_SELECTCANDIDATESTR"></a><a id="ni_selectcandidatestr"></a><dl>
<dt><b>NI_SELECTCANDIDATESTR</b></dt>
</dl>
</td>
<td width="60%">
An application has selected one of the candidates. The <i>dwIndex</i> parameter specifies an index of a candidate list to be selected. The <i>dwValue</i> parameter specifies an index of a candidate string in the selected candidate list.

</td>
</tr>
<tr>
<td width="40%"><a id="NI_SETCANDIDATE_PAGESIZE"></a><a id="ni_setcandidate_pagesize"></a><dl>
<dt><b>NI_SETCANDIDATE_PAGESIZE</b></dt>
</dl>
</td>
<td width="60%">
The application changes the page size of a candidate list. The <i>dwIndex</i> parameter specifies the candidate list to be changed and must have a value in the range 0 to 3. The <i>dwValue</i> parameter specifies the new page size.

</td>
</tr>
<tr>
<td width="40%"><a id="NI_SETCANDIDATE_PAGESTART"></a><a id="ni_setcandidate_pagestart"></a><dl>
<dt><b>NI_SETCANDIDATE_PAGESTART</b></dt>
</dl>
</td>
<td width="60%">
The application changes the page starting index of a candidate list. The <i>dwIndex</i> parameter specifies the candidate list to be changed and must have a value in the range 0 to 3. The <i>dwValue</i> parameter specifies the new page start index.

</td>
</tr>
</table>

### -param dwIndex [in]

Index of a candidate list. Alternatively, if <i>dwAction</i> is NI_COMPOSITIONSTR, this parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CPS_CANCEL"></a><a id="cps_cancel"></a><dl>
<dt><b>CPS_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
Clear the composition string and set the status to no composition string.

</td>
</tr>
<tr>
<td width="40%"><a id="CPS_COMPLETE"></a><a id="cps_complete"></a><dl>
<dt><b>CPS_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Set the composition string as the result string.

</td>
</tr>
<tr>
<td width="40%"><a id="CPS_CONVERT"></a><a id="cps_convert"></a><dl>
<dt><b>CPS_CONVERT</b></dt>
</dl>
</td>
<td width="60%">
Convert the composition string.

</td>
</tr>
<tr>
<td width="40%"><a id="CPS_REVERT"></a><a id="cps_revert"></a><dl>
<dt><b>CPS_REVERT</b></dt>
</dl>
</td>
<td width="60%">
Cancel the current composition string and set the composition string to be the unconverted string.

</td>
</tr>
</table>

### -param dwValue [in]

Index of a candidate string. The application can set this parameter or ignore it, depending on the value of the <i>dwAction</i> parameter.

## -returns

Returns nonzero if successful, or 0 otherwise.

## -see-also

<a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a>



<a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
