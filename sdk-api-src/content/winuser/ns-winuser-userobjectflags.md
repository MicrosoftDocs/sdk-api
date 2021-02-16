---
UID: NS:winuser.tagUSEROBJECTFLAGS
title: USEROBJECTFLAGS (winuser.h)
description: Contains information about a window station or desktop handle.
helpviewer_keywords: ["*PUSEROBJECTFLAGS","DF_ALLOWOTHERACCOUNTHOOK","PUSEROBJECTFLAGS","PUSEROBJECTFLAGS structure pointer [Windows Stations and Desktops]","USEROBJECTFLAGS","USEROBJECTFLAGS structure [Windows Stations and Desktops]","WSF_VISIBLE","_win32_userobjectflags_str","base.userobjectflags_str","tagUSEROBJECTFLAGS","winstation.userobjectflags_str","winuser/PUSEROBJECTFLAGS","winuser/USEROBJECTFLAGS"]
old-location: winstation\userobjectflags_str.htm
tech.root: winstation
ms.assetid: 5a973d45-5ff4-47e7-a927-72d3fdd61dc9
ms.date: 12/05/2018
ms.keywords: '*PUSEROBJECTFLAGS, DF_ALLOWOTHERACCOUNTHOOK, PUSEROBJECTFLAGS, PUSEROBJECTFLAGS structure pointer [Windows Stations and Desktops], USEROBJECTFLAGS, USEROBJECTFLAGS structure [Windows Stations and Desktops], WSF_VISIBLE, _win32_userobjectflags_str, base.userobjectflags_str, tagUSEROBJECTFLAGS, winstation.userobjectflags_str, winuser/PUSEROBJECTFLAGS, winuser/USEROBJECTFLAGS'
req.header: winuser.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: USEROBJECTFLAGS, *PUSEROBJECTFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUSEROBJECTFLAGS
 - winuser/tagUSEROBJECTFLAGS
 - PUSEROBJECTFLAGS
 - winuser/PUSEROBJECTFLAGS
 - USEROBJECTFLAGS
 - winuser/USEROBJECTFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - USEROBJECTFLAGS
---

# USEROBJECTFLAGS structure


## -description

Contains information about a window station or desktop handle.

## -struct-fields

### -field fInherit

If this member is TRUE, new processes inherit the handle. Otherwise, the handle is not inherited.

### -field fReserved

Reserved for future use. This member must be FALSE.

### -field dwFlags

For window stations, this member can contain the following window station attribute.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WSF_VISIBLE"></a><a id="wsf_visible"></a><dl>
<dt><b>WSF_VISIBLE</b></dt>
<dt>0x0001L</dt>
</dl>
</td>
<td width="60%">
Window station has visible display surfaces.

</td>
</tr>
</table>
 

For desktops, the <b>dwFlags</b> member can contain the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DF_ALLOWOTHERACCOUNTHOOK"></a><a id="df_allowotheraccounthook"></a><dl>
<dt><b>DF_ALLOWOTHERACCOUNTHOOK</b></dt>
<dt>0x0001L</dt>
</dl>
</td>
<td width="60%">
Allows processes running in other accounts on the desktop to set hooks in this process.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa">GetUserObjectInformation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-opendesktopa">OpenDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-openinputdesktop">OpenInputDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setuserobjectinformationa">SetUserObjectInformation</a>