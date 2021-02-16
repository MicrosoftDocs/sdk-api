---
UID: NS:msacm.tACMFILTERCHOOSE
title: ACMFILTERCHOOSE (msacm.h)
description: The ACMFILTERCHOOSE structure contains information the ACM uses to initialize the system-defined waveform-audio filter selection dialog box.
helpviewer_keywords: ["*LPACMFILTERCHOOSE","*PACMFILTERCHOOSE","ACMFILTERCHOOSE","ACMFILTERCHOOSE structure [Windows Multimedia]","ACMFILTERCHOOSE_STYLEF_CONTEXTHELP","ACMFILTERCHOOSE_STYLEF_ENABLEHOOK","ACMFILTERCHOOSE_STYLEF_ENABLETEMPLATE","ACMFILTERCHOOSE_STYLEF_ENABLETEMPLATEHANDLE","ACMFILTERCHOOSE_STYLEF_INITTOFILTERSTRUCT","ACMFILTERCHOOSE_STYLEF_SHOWHELP","ACM_FILTERENUMF_DWFILTERTAG","msacm/ACMFILTERCHOOSE","multimedia.acmfilterchoose_COLLISION925","multimedia.acmfilterchoose_struct"]
old-location: multimedia\acmfilterchoose_struct.htm
tech.root: Multimedia
ms.assetid: 92ec2a41-e853-4533-b831-43c9d52dc27f
ms.date: 12/05/2018
ms.keywords: '*LPACMFILTERCHOOSE, *PACMFILTERCHOOSE, ACMFILTERCHOOSE, ACMFILTERCHOOSE structure [Windows Multimedia], ACMFILTERCHOOSE_STYLEF_CONTEXTHELP, ACMFILTERCHOOSE_STYLEF_ENABLEHOOK, ACMFILTERCHOOSE_STYLEF_ENABLETEMPLATE, ACMFILTERCHOOSE_STYLEF_ENABLETEMPLATEHANDLE, ACMFILTERCHOOSE_STYLEF_INITTOFILTERSTRUCT, ACMFILTERCHOOSE_STYLEF_SHOWHELP, ACM_FILTERENUMF_DWFILTERTAG, msacm/ACMFILTERCHOOSE, multimedia.acmfilterchoose_COLLISION925, multimedia.acmfilterchoose_struct'
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
req.typenames: ACMFILTERCHOOSE, *PACMFILTERCHOOSE, *LPACMFILTERCHOOSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tACMFILTERCHOOSE
 - msacm/tACMFILTERCHOOSE
 - PACMFILTERCHOOSE
 - msacm/PACMFILTERCHOOSE
 - ACMFILTERCHOOSE
 - msacm/ACMFILTERCHOOSE
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
 - ACMFILTERCHOOSE
---

# ACMFILTERCHOOSE structure


## -description

The <b>ACMFILTERCHOOSE</b> structure contains information the ACM uses to initialize the system-defined waveform-audio filter selection dialog box. After the user closes the dialog box, the system returns information about the user's selection in this structure.

## -struct-fields

### -field cbStruct

Size, in bytes, of the <b>ACMFILTERCHOOSE</b> structure. This member must be initialized before an application calls the <a href="/windows/desktop/api/msacm/nf-msacm-acmfilterchoose">acmFilterChoose</a> function. The size specified in this member must be large enough to contain the base <b>ACMFILTERCHOOSE</b> structure.

### -field fdwStyle

Optional style flags for the <a href="/windows/desktop/api/msacm/nf-msacm-acmfilterchoose">acmFilterChoose</a> function. This member must be initialized to a valid combination of the following flags before an application calls the <b>acmFilterChoose</b> function. The following values are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ACMFILTERCHOOSE_STYLEF_CONTEXTHELP"></a><a id="acmfilterchoose_stylef_contexthelp"></a><dl>
<dt><b>ACMFILTERCHOOSE_STYLEF_CONTEXTHELP</b></dt>
</dl>
</td>
<td width="60%">
Context-sensitive help will be available in the dialog box. To use this feature, an application must register the ACMHELPMSGCONTEXTMENU and ACMHELPMSGCONTEXTHELP constants, using the <a href="/windows/win32/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a> function. When the user invokes help, the registered message will be posted to the owning window. The message will contain the <i>wParam</i> and <i>lParam</i> parameters from the original WM_CONTEXTMENU or WM_CONTEXTHELP message.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMFILTERCHOOSE_STYLEF_ENABLEHOOK"></a><a id="acmfilterchoose_stylef_enablehook"></a><dl>
<dt><b>ACMFILTERCHOOSE_STYLEF_ENABLEHOOK</b></dt>
</dl>
</td>
<td width="60%">
Enables the hook function specified in the <b>pfnHook</b> member. An application can use hook functions for a variety of customizations, including answering the <a href="/windows/desktop/Multimedia/mm-acm-filterchoose">MM_ACM_FILTERCHOOSE</a> message.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMFILTERCHOOSE_STYLEF_ENABLETEMPLATE"></a><a id="acmfilterchoose_stylef_enabletemplate"></a><dl>
<dt><b>ACMFILTERCHOOSE_STYLEF_ENABLETEMPLATE</b></dt>
</dl>
</td>
<td width="60%">
Causes the ACM to create the dialog box template identified by the <b>hInstance</b> and <b>pszTemplateName</b> members.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMFILTERCHOOSE_STYLEF_ENABLETEMPLATEHANDLE"></a><a id="acmfilterchoose_stylef_enabletemplatehandle"></a><dl>
<dt><b>ACMFILTERCHOOSE_STYLEF_ENABLETEMPLATEHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <b>hInstance</b> member identifies a data block that contains a preloaded dialog box template. If this flag is specified, the ACM ignores the <b>pszTemplateName</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMFILTERCHOOSE_STYLEF_INITTOFILTERSTRUCT"></a><a id="acmfilterchoose_stylef_inittofilterstruct"></a><dl>
<dt><b>ACMFILTERCHOOSE_STYLEF_INITTOFILTERSTRUCT</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <b>pwfltr</b> contains a valid <a href="/windows/desktop/api/mmreg/ns-mmreg-wavefilter">WAVEFILTER</a> structure that the dialog box will use as the initial selection.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMFILTERCHOOSE_STYLEF_SHOWHELP"></a><a id="acmfilterchoose_stylef_showhelp"></a><dl>
<dt><b>ACMFILTERCHOOSE_STYLEF_SHOWHELP</b></dt>
</dl>
</td>
<td width="60%">
A help button will appear in the dialog box. To use a custom Help file, an application must register the ACMHELPMSGSTRING value with the <a href="/windows/win32/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a> function. When the user presses the help button, the registered message is posted to the owner.

</td>
</tr>
</table>

### -field hwndOwner

Handle to the window that owns the dialog box. This member can be any valid window handle or <b>NULL</b> if the dialog box has no owner. This member must be initialized before calling the <a href="/windows/desktop/api/msacm/nf-msacm-acmfilterchoose">acmFilterChoose</a> function.

### -field pwfltr

Pointer to a <a href="/windows/desktop/api/mmreg/ns-mmreg-wavefilter">WAVEFILTER</a> structure. If the ACMFILTERCHOOSE_STYLEF_INITTOFILTERSTRUCT flag is specified in the <b>fdwStyle</b> member, this structure must be initialized to a valid filter. When the <a href="/windows/desktop/api/msacm/nf-msacm-acmfilterchoose">acmFilterChoose</a> function returns, this buffer contains the selected filter. If the user cancels the dialog box, no changes will be made to this buffer.

### -field cbwfltr

Size, in bytes, of the buffer pointed to by the <b>pwfltr</b> member. The <a href="/windows/desktop/api/msacm/nf-msacm-acmfilterchoose">acmFilterChoose</a> function returns ACMERR_NOTPOSSIBLE if the buffer is too small to contain the filter information; the ACM also copies the required size into this member. An application can use the <a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a> and <a href="/windows/desktop/api/msacm/nf-msacm-acmfiltertagdetails">acmFilterTagDetails</a> functions to determine the largest size required for this buffer.

### -field pszTitle

Pointer to a string to be placed in the title bar of the dialog box. If this member is <b>NULL</b>, the ACM uses the default title (that is, "Filter Selection").

### -field szFilterTag

Buffer containing a null-terminated string describing the filter tag of the filter selection when the [ACMFILTERTAGDETAILS](./nf-msacm-acmfiltertagdetails.md) structure returned by <a href="/windows/desktop/api/msacm/nf-msacm-acmfiltertagdetails">acmFilterTagDetails</a>. If the user cancels the dialog box, this member will contain a null-terminated string.

### -field szFilter

Buffer containing a null-terminated string describing the filter attributes of the filter selection when the [ACMFILTERDETAILS](./nf-msacm-acmfilterdetails.md) structure returned by <a href="/windows/desktop/api/msacm/nf-msacm-acmfilterdetails">acmFilterDetails</a>. If the user cancels the dialog box, this member will contain a null-terminated string.

### -field pszName

Pointer to a string for a user-defined filter name. If this is a non-null-terminated string, the ACM attempts to match the name with a previously saved user-defined filter name. If a match is found, the dialog box is initialized to that filter. If a match is not found or this member is a null-terminated string, this member is ignored for input. When the <a href="/windows/desktop/api/msacm/nf-msacm-acmfilterchoose">acmFilterChoose</a> function returns, this buffer contains a null-terminated string describing the user-defined filter. If the filter name is untitled (that is, the user has not given a name for the filter), this member will be a null-terminated string on return. If the user cancels the dialog box, no changes will be made to this buffer.

If the ACMFILTERCHOOSE_STYLEF_INITTOFILTERSTRUCT flag is specified by the <b>fdwStyle</b> member, the <b>pszName</b> member is ignored as an input member.

### -field cchName

Size, in characters, of the buffer identified by the <b>pszName</b> member. This buffer should be at least 128 characters long. If <b>pszName</b> is <b>NULL</b>, this member is ignored.

### -field fdwEnum

Optional flags for restricting the type of filters listed in the dialog box. These flags are identical to the <i>fdwEnum</i> flags for the <a href="/windows/desktop/api/msacm/nf-msacm-acmfilterenum">acmFilterEnum</a> function. If <b>pwfltrEnum</b> is <b>NULL</b>, this member should be zero.

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ACM_FILTERENUMF_DWFILTERTAG"></a><a id="acm_filterenumf_dwfiltertag"></a><dl>
<dt><b>ACM_FILTERENUMF_DWFILTERTAG</b></dt>
</dl>
</td>
<td width="60%">
The <b>dwFilterTag</b> member of the <a href="/windows/desktop/api/mmreg/ns-mmreg-wavefilter">WAVEFILTER</a> structure pointed to by the <b>pwfltrEnum</b> member is valid. The enumerator will only enumerate a filter that conforms to this attribute.

</td>
</tr>
</table>

### -field pwfltrEnum

Pointer to a <a href="/windows/desktop/api/mmreg/ns-mmreg-wavefilter">WAVEFILTER</a> structure that will be used to restrict the filters listed in the dialog box. The <b>fdwEnum</b> member defines which members of this structure should be used for the enumeration restrictions. The <b>cbStruct</b> member of this <b>WAVEFILTER</b> structure must be initialized to the size of the <b>WAVEFILTER</b> structure. If no special restrictions are desired, this member can be <b>NULL</b>.

### -field hInstance

Handle to a data block that contains a dialog box template specified by the <b>pszTemplateName</b> member. This member is used only if the <b>fdwStyle</b> member specifies the ACMFILTERCHOOSE_STYLEF_ENABLETEMPLATE or ACMFILTERCHOOSE_STYLEF_ENABLETEMPLATEHANDLE flag; otherwise, this member should be <b>NULL</b> on input.

### -field pszTemplateName

Pointer to a null-terminated string that specifies the name of the resource file for the dialog box template that is to be substituted for the dialog box template in the ACM. An application can use the <a href="/windows/win32/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro for numbered dialog box resources. This member is used only if the <b>fdwStyle</b> member specifies the ACMFILTERCHOOSE_STYLEF_ENABLETEMPLATE flag; otherwise, this member should be <b>NULL</b> on input.

### -field lCustData

Application-defined data that the ACM passes to the hook function identified by the <b>pfnHook</b> member. The system passes the data in the <i>lParam</i> parameter of the <a href="/windows/win32/dlgbox/wm-initdialog">WM_INITDIALOG</a> message.

### -field pfnHook

Pointer to a callback function that processes messages intended for the dialog box. An application must specify the ACMFILTERCHOOSE_STYLEF_ENABLEHOOK flag in the <b>fdwStyle</b> member to enable the hook; otherwise, this member should be <b>NULL</b>. The hook function should return <b>FALSE</b> to pass a message to the standard dialog box procedure or <b>TRUE</b> to discard the message. The callback function type is <a href="/windows/desktop/api/msacm/nc-msacm-acmfilterchoosehookproc">acmFilterChooseHookProc</a>.

## -see-also

[ACMFILTERDETAILS](./nf-msacm-acmfilterdetails.md)



[ACMFILTERTAGDETAILS](./nf-msacm-acmfiltertagdetails.md)



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>



<a href="/windows/desktop/Multimedia/audio-compression-structures">Audio Compression Structures</a>



<a href="/windows/win32/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<a href="/windows/desktop/Multimedia/mm-acm-filterchoose">MM_ACM_FILTERCHOOSE</a>



<a href="/windows/win32/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a>



<a href="/windows/desktop/api/mmreg/ns-mmreg-wavefilter">WAVEFILTER</a>



<a href="/windows/win32/dlgbox/wm-initdialog">WM_INITDIALOG</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmfilterchoose">acmFilterChoose</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmfilterdetails">acmFilterDetails</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmfilterenum">acmFilterEnum</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmfiltertagdetails">acmFilterTagDetails</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a>