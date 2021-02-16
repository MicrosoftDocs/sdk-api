---
UID: NS:msacm.tACMFORMATCHOOSE
title: ACMFORMATCHOOSE (msacm.h)
description: The ACMFORMATCHOOSE structure contains information the ACM uses to initialize the system-defined waveform-audio format selection dialog box.
helpviewer_keywords: ["*LPACMFORMATCHOOSE","*PACMFORMATCHOOSE","ACMFORMATCHOOSE","ACMFORMATCHOOSE structure [Windows Multimedia]","ACMFORMATCHOOSE_STYLEF_CONTEXTHELP","ACMFORMATCHOOSE_STYLEF_ENABLEHOOK","ACMFORMATCHOOSE_STYLEF_ENABLETEMPLATE","ACMFORMATCHOOSE_STYLEF_ENABLETEMPLATEHANDLE","ACMFORMATCHOOSE_STYLEF_INITTOWFXSTRUCT","ACMFORMATCHOOSE_STYLEF_SHOWHELP","ACM_FORMATENUMF_CONVERT","ACM_FORMATENUMF_HARDWARE","ACM_FORMATENUMF_INPUT","ACM_FORMATENUMF_NCHANNELS","ACM_FORMATENUMF_NSAMPLESPERSEC","ACM_FORMATENUMF_OUTPUT","ACM_FORMATENUMF_SUGGEST","ACM_FORMATENUMF_WBITSPERSAMPLE","ACM_FORMATENUMF_WFORMATTAG","msacm/ACMFORMATCHOOSE","multimedia.acmformatchoose_struct"]
old-location: multimedia\acmformatchoose_struct.htm
tech.root: Multimedia
ms.assetid: b5e36dbd-9eaf-479a-af4c-ce07e4b6f042
ms.date: 12/05/2018
ms.keywords: '*LPACMFORMATCHOOSE, *PACMFORMATCHOOSE, ACMFORMATCHOOSE, ACMFORMATCHOOSE structure [Windows Multimedia], ACMFORMATCHOOSE_STYLEF_CONTEXTHELP, ACMFORMATCHOOSE_STYLEF_ENABLEHOOK, ACMFORMATCHOOSE_STYLEF_ENABLETEMPLATE, ACMFORMATCHOOSE_STYLEF_ENABLETEMPLATEHANDLE, ACMFORMATCHOOSE_STYLEF_INITTOWFXSTRUCT, ACMFORMATCHOOSE_STYLEF_SHOWHELP, ACM_FORMATENUMF_CONVERT, ACM_FORMATENUMF_HARDWARE, ACM_FORMATENUMF_INPUT, ACM_FORMATENUMF_NCHANNELS, ACM_FORMATENUMF_NSAMPLESPERSEC, ACM_FORMATENUMF_OUTPUT, ACM_FORMATENUMF_SUGGEST, ACM_FORMATENUMF_WBITSPERSAMPLE, ACM_FORMATENUMF_WFORMATTAG, msacm/ACMFORMATCHOOSE, multimedia.acmformatchoose_struct'
req.header: msacm.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ACMFORMATCHOOSE, *PACMFORMATCHOOSE, *LPACMFORMATCHOOSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tACMFORMATCHOOSE
 - msacm/tACMFORMATCHOOSE
 - PACMFORMATCHOOSE
 - msacm/PACMFORMATCHOOSE
 - ACMFORMATCHOOSE
 - msacm/ACMFORMATCHOOSE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msacm.h
api_name:
 - ACMFORMATCHOOSE
---

# ACMFORMATCHOOSE structure


## -description

The <b>ACMFORMATCHOOSE</b> structure contains information the ACM uses to initialize the system-defined waveform-audio format selection dialog box. After the user closes the dialog box, the system returns information about the user's selection in this structure.

## -struct-fields

### -field cbStruct

Size, in bytes, of the <b>ACMFORMATCHOOSE</b> structure. This member must be initialized before an application calls the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatchoose">acmFormatChoose</a> function. The size specified in this member must be large enough to contain the base <b>ACMFORMATCHOOSE</b> structure.

### -field fdwStyle

Optional style flags for the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatchoose">acmFormatChoose</a> function. This member must be initialized to a valid combination of the following flags before an application calls the <b>acmFormatChoose</b> function:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ACMFORMATCHOOSE_STYLEF_CONTEXTHELP"></a><a id="acmformatchoose_stylef_contexthelp"></a><dl>
<dt><b>ACMFORMATCHOOSE_STYLEF_CONTEXTHELP</b></dt>
</dl>
</td>
<td width="60%">
Context-sensitive help will be available in the dialog box. To use this feature, an application must register the ACMHELPMSGCONTEXTMENU and ACMHELPMSGCONTEXTHELP constants, using the <a href="/windows/win32/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a> function. When the user invokes help, the registered message will be posted to the owning window. The message will contain the <i>wParam</i> and <i>lParam</i> parameters from the original WM_CONTEXTMENU or WM_CONTEXTHELP message.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMFORMATCHOOSE_STYLEF_ENABLEHOOK"></a><a id="acmformatchoose_stylef_enablehook"></a><dl>
<dt><b>ACMFORMATCHOOSE_STYLEF_ENABLEHOOK</b></dt>
</dl>
</td>
<td width="60%">
Enables the hook function pointed to by the <b>pfnHook</b> member. An application can use hook functions for a variety of customizations, including answering the <a href="/windows/desktop/Multimedia/mm-acm-formatchoose">MM_ACM_FORMATCHOOSE</a> message.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMFORMATCHOOSE_STYLEF_ENABLETEMPLATE"></a><a id="acmformatchoose_stylef_enabletemplate"></a><dl>
<dt><b>ACMFORMATCHOOSE_STYLEF_ENABLETEMPLATE</b></dt>
</dl>
</td>
<td width="60%">
Causes the ACM to create the dialog box template identified by <b>hInstance</b> and <b>pszTemplateName</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMFORMATCHOOSE_STYLEF_ENABLETEMPLATEHANDLE"></a><a id="acmformatchoose_stylef_enabletemplatehandle"></a><dl>
<dt><b>ACMFORMATCHOOSE_STYLEF_ENABLETEMPLATEHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <b>hInstance</b> member identifies a data block that contains a preloaded dialog box template. If this flag is specified, the ACM ignores the <b>pszTemplateName</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMFORMATCHOOSE_STYLEF_INITTOWFXSTRUCT"></a><a id="acmformatchoose_stylef_inittowfxstruct"></a><dl>
<dt><b>ACMFORMATCHOOSE_STYLEF_INITTOWFXSTRUCT</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <b>pwfx</b> contains a valid <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that the dialog box will use as the initial selection.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMFORMATCHOOSE_STYLEF_SHOWHELP"></a><a id="acmformatchoose_stylef_showhelp"></a><dl>
<dt><b>ACMFORMATCHOOSE_STYLEF_SHOWHELP</b></dt>
</dl>
</td>
<td width="60%">
A help button will appear in the dialog box. To use a custom Help file, an application must register the ACMHELPMSGSTRING constant with the <a href="/windows/win32/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a> function. When the user presses the help button, the registered message will be posted to the owner.

</td>
</tr>
</table>

### -field hwndOwner

Handle to the window that owns the dialog box. This member can be any valid window handle, or <b>NULL</b> if the dialog box has no owner. This member must be initialized before calling the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatchoose">acmFormatChoose</a> function.

### -field pwfx

Pointer to a <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure. If the ACMFORMATCHOOSE_STYLEF_INITTOWFXSTRUCT flag is specified in the <b>fdwStyle</b> member, this structure must be initialized to a valid format. When the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatchoose">acmFormatChoose</a> function returns, this buffer contains the selected format. If the user cancels the dialog box, no changes will be made to this buffer.

### -field cbwfx

Size, in bytes, of the buffer pointed to by <b>pwfx</b>. If the buffer is too small to contain the format information, the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatchoose">acmFormatChoose</a> function returns ACMERR_NOTPOSSIBLE. Also, the ACM copies the required size into this member. An application can use the <a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a> and <a href="/windows/desktop/api/msacm/nf-msacm-acmformattagdetails">acmFormatTagDetails</a> functions to determine the largest size required for this buffer.

### -field pszTitle

Pointer to a string to be placed in the title bar of the dialog box. If this member is <b>NULL</b>, the ACM uses the default title (that is, "Sound Selection").

### -field szFormatTag

Buffer containing a null-terminated string describing the format tag of the format selection when the [ACMFORMATTAGDETAILS](./nf-msacm-acmformattagdetails.md) structure returned by the <a href="/windows/desktop/api/msacm/nf-msacm-acmformattagdetails">acmFormatTagDetails</a> function. If the user cancels the dialog box, this member will contain a null-terminated string.

### -field szFormat

Buffer containing a null-terminated string describing the format attributes of the format selection when the [ACMFORMATDETAILS](./nf-msacm-acmformatdetails.md) structure returned by the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatdetails">acmFormatDetails</a> function. If the user cancels the dialog box, this member will contain a null-terminated string.

### -field pszName

Pointer to a string for a user-defined format name. If this is a non-null-terminated string, the ACM will attempt to match the name with a previously saved user-defined format name. If a match is found, the dialog box is initialized to that format. If a match is not found or this member is a null-terminated string, this member is ignored on input. When the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatchoose">acmFormatChoose</a> function returns, this buffer contains a null-terminated string describing the user-defined format. If the format name is untitled (that is, the user has not given a name for the format), this member will be a null-terminated string on return. If the user cancels the dialog box, no changes will be made to this buffer.

### -field cchName

Size, in characters, of the buffer identified by the <b>pszName</b> member. This buffer should be at least 128 characters long. If the <b>pszName</b> member is <b>NULL</b>, this member is ignored.

### -field fdwEnum

Optional flags for restricting the type of formats listed in the dialog box. These flags are identical to the <i>fdwEnum</i> flags for the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatenum">acmFormatEnum</a> function. If <b>pwfxEnum</b> is <b>NULL</b>, this member should be zero. The following values are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ACM_FORMATENUMF_CONVERT"></a><a id="acm_formatenumf_convert"></a><dl>
<dt><b>ACM_FORMATENUMF_CONVERT</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure pointed to by the <b>pwfxEnum</b> member is valid. The enumerator will enumerate only destination formats that can be converted from the given <b>pwfxEnum</b> format.

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_FORMATENUMF_HARDWARE"></a><a id="acm_formatenumf_hardware"></a><dl>
<dt><b>ACM_FORMATENUMF_HARDWARE</b></dt>
</dl>
</td>
<td width="60%">
The enumerator should enumerate only formats that are supported in hardware by one or more of the installed waveform-audio devices. This flag provides a way for an application to choose only formats native to an installed waveform-audio device.

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_FORMATENUMF_INPUT"></a><a id="acm_formatenumf_input"></a><dl>
<dt><b>ACM_FORMATENUMF_INPUT</b></dt>
</dl>
</td>
<td width="60%">
The enumerator should enumerate only formats that are supported for input (recording).

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_FORMATENUMF_NCHANNELS"></a><a id="acm_formatenumf_nchannels"></a><dl>
<dt><b>ACM_FORMATENUMF_NCHANNELS</b></dt>
</dl>
</td>
<td width="60%">
The <b>nChannels</b> member of the <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure pointed to by the <b>pwfxEnum</b> member is valid. The enumerator will enumerate only a format that conforms to this attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_FORMATENUMF_NSAMPLESPERSEC"></a><a id="acm_formatenumf_nsamplespersec"></a><dl>
<dt><b>ACM_FORMATENUMF_NSAMPLESPERSEC</b></dt>
</dl>
</td>
<td width="60%">
The <b>nSamplesPerSec</b> member of the <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure pointed to by the <b>pwfxEnum</b> member is valid. The enumerator will enumerate only a format that conforms to this attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_FORMATENUMF_OUTPUT"></a><a id="acm_formatenumf_output"></a><dl>
<dt><b>ACM_FORMATENUMF_OUTPUT</b></dt>
</dl>
</td>
<td width="60%">
The enumerator should enumerate only formats that are supported for output (playback).

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_FORMATENUMF_SUGGEST"></a><a id="acm_formatenumf_suggest"></a><dl>
<dt><b>ACM_FORMATENUMF_SUGGEST</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure pointed to by the <b>pwfxEnum</b> member is valid. The enumerator will enumerate all suggested destination formats for the given <b>pwfxEnum</b> format.

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_FORMATENUMF_WBITSPERSAMPLE"></a><a id="acm_formatenumf_wbitspersample"></a><dl>
<dt><b>ACM_FORMATENUMF_WBITSPERSAMPLE</b></dt>
</dl>
</td>
<td width="60%">
The <b>wBitsPerSample</b> member of the <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure pointed to by the <b>pwfxEnum</b> member is valid. The enumerator will enumerate only a format that conforms to this attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_FORMATENUMF_WFORMATTAG"></a><a id="acm_formatenumf_wformattag"></a><dl>
<dt><b>ACM_FORMATENUMF_WFORMATTAG</b></dt>
</dl>
</td>
<td width="60%">
The <b>wFormatTag</b> member of the <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure pointed to by the <b>pwfxEnum</b> member is valid. The enumerator will enumerate only a format that conforms to this attribute.

</td>
</tr>
</table>

### -field pwfxEnum

Pointer to a <b>WAVEFORMATEX</b> structure that will be used to restrict the formats listed in the dialog box. The <b>fdwEnum</b> member defines the members of the structure pointed to by <b>pwfxEnum</b> that should be used for the enumeration restrictions. If no special restrictions are desired, this member can be <b>NULL</b>. For other requirements associated with the <b>pwfxEnum</b> member, see the description for the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatenum">acmFormatEnum</a> function.

### -field hInstance

Handle to a data block that contains a dialog box template specified by the <b>pszTemplateName</b> member. This member is used only if the <b>fdwStyle</b> member specifies the ACMFORMATCHOOSE_STYLEF_ENABLETEMPLATE or ACMFORMATCHOOSE_STYLEF_ENABLETEMPLATEHANDLE flag; otherwise, this member should be <b>NULL</b> on input.

### -field pszTemplateName

Pointer to a null-terminated string that specifies the name of the resource file for the dialog box template that is to be substituted for the dialog box template in the ACM. An application can use the <a href="/windows/win32/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro for numbered dialog box resources. This member is used only if the <b>fdwStyle</b> member specifies the ACMFORMATCHOOSE_STYLEF_ENABLETEMPLATE flag; otherwise, this member should be <b>NULL</b> on input.

### -field lCustData

Application-defined data that the ACM passes to the hook function identified by the <b>pfnHook</b> member. The system passes the data in the <i>lParam</i> parameter of the <a href="/windows/win32/dlgbox/wm-initdialog">WM_INITDIALOG</a> message.

### -field pfnHook

Pointer to a callback function that processes messages intended for the dialog box. An application must specify the ACMFORMATCHOOSE_STYLEF_ENABLEHOOK flag in the <b>fdwStyle</b> member to enable the hook; otherwise, this member should be <b>NULL</b>. The hook function should return <b>FALSE</b> to pass a message to the standard dialog box procedure or <b>TRUE</b> to discard the message. The callback function type is <a href="/windows/desktop/api/msacm/nc-msacm-acmformatchoosehookproc">acmFormatChooseHookProc</a>.

## -see-also

[ACMFORMATDETAILS](./nf-msacm-acmformatdetails.md)



[ACMFORMATTAGDETAILS](./nf-msacm-acmformattagdetails.md)



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>



<a href="/windows/desktop/Multimedia/audio-compression-structures">Audio Compression Structures</a>



<a href="/windows/win32/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<a href="/windows/desktop/Multimedia/mm-acm-formatchoose">MM_ACM_FORMATCHOOSE</a>



<a href="/windows/win32/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a>



<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a>



<a href="/windows/win32/dlgbox/wm-initdialog">WM_INITDIALOG</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmformatchoose">acmFormatChoose</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmformatdetails">acmFormatDetails</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmformatenum">acmFormatEnum</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmformattagdetails">acmFormatTagDetails</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a>