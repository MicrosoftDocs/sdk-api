---
UID: NS:winnetwk._DISCDLGSTRUCTA
title: DISCDLGSTRUCTA (winnetwk.h)
description: Used in the WNetDisconnectDialog1 function. The structure contains required information for the disconnect attempt. (ANSI)
helpviewer_keywords: ["*LPDISCDLGSTRUCTA","DISCDLGSTRUCT","DISCDLGSTRUCT structure [Windows Networking (WNet)]","DISCDLGSTRUCTA","DISCDLGSTRUCTW","DISC_NO_FORCE","DISC_UPDATE_PROFILE","LPDISCDLGSTRUCT","LPDISCDLGSTRUCT structure pointer [Windows Networking (WNet)]","_win32_discdlgstruct_str","winnetwk/DISCDLGSTRUCT","winnetwk/DISCDLGSTRUCTA","winnetwk/DISCDLGSTRUCTW","winnetwk/LPDISCDLGSTRUCT","wnet.discdlgstruct_str"]
old-location: wnet\discdlgstruct_str.htm
tech.root: WNet
ms.assetid: ae415815-f247-4217-a4f1-6a7ca9288890
ms.date: 12/05/2018
ms.keywords: '*LPDISCDLGSTRUCTA, DISCDLGSTRUCT, DISCDLGSTRUCT structure [Windows Networking (WNet)], DISCDLGSTRUCTA, DISCDLGSTRUCTW, DISC_NO_FORCE, DISC_UPDATE_PROFILE, LPDISCDLGSTRUCT, LPDISCDLGSTRUCT structure pointer [Windows Networking (WNet)], _win32_discdlgstruct_str, winnetwk/DISCDLGSTRUCT, winnetwk/DISCDLGSTRUCTA, winnetwk/DISCDLGSTRUCTW, winnetwk/LPDISCDLGSTRUCT, wnet.discdlgstruct_str'
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DISCDLGSTRUCTW (Unicode) and DISCDLGSTRUCTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DISCDLGSTRUCTA, *LPDISCDLGSTRUCTA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DISCDLGSTRUCTA
 - winnetwk/_DISCDLGSTRUCTA
 - LPDISCDLGSTRUCTA
 - winnetwk/LPDISCDLGSTRUCTA
 - DISCDLGSTRUCTA
 - winnetwk/DISCDLGSTRUCTA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnetwk.h
api_name:
 - DISCDLGSTRUCT
 - DISCDLGSTRUCTA
 - DISCDLGSTRUCTW
---

# DISCDLGSTRUCTA structure


## -description

The
				<b>DISCDLGSTRUCT</b> structure is used in the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetdisconnectdialog1a">WNetDisconnectDialog1</a> function. The structure contains required information for the disconnect attempt.

## -struct-fields

### -field cbStructure

Type: <b>DWORD</b>

The size, in bytes, of the 
<b>DISCDLGSTRUCT</b> structure. The caller must supply this value.

### -field hwndOwner

Type: <b>HWND</b>

A handle to the owner window of the dialog box.

### -field lpLocalName

Type: <b>LPTSTR</b>

A pointer to a <b>NULL</b>-terminated  string that specifies the local device name that is redirected to the network resource, such as "F:" or "LPT1".

### -field lpRemoteName

Type: <b>LPTSTR</b>

A pointer to a <b>NULL</b>-terminated  string that specifies the name of the network resource to disconnect. This member can be NULL if the <b>lpLocalName</b> member is specified. When <b>lpLocalName</b> is specified, the connection to the network resource redirected from <b>lpLocalName</b>  is disconnected.

### -field dwFlags

Type: <b>DWORD</b>

A set of bit flags describing the connection. This member can be a combination of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISC_UPDATE_PROFILE"></a><a id="disc_update_profile"></a><dl>
<dt><b>DISC_UPDATE_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
If this value is set, the specified connection is no longer a persistent one (automatically restored every time the user logs on). This flag is valid only if the <b>lpLocalName</b> member specifies a local device.

</td>
</tr>
<tr>
<td width="40%"><a id="DISC_NO_FORCE"></a><a id="disc_no_force"></a><dl>
<dt><b>DISC_NO_FORCE</b></dt>
</dl>
</td>
<td width="60%">
If this value is not set, the system applies force when attempting to disconnect from the network resource. 




This situation typically occurs when the user has files open over the connection. This value means that the user will be informed if there are open files on the connection, and asked if he or she still wants to disconnect. If the user wants to proceed, the disconnect procedure re-attempts with additional force.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetdisconnectdialog1a">WNetDisconnectDialog1</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-structures">Windows Networking Structures</a>

## -remarks

> [!NOTE]
> The winnetwk.h header defines DISCDLGSTRUCT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
