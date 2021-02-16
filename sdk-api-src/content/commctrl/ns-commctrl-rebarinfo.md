---
UID: NS:commctrl.tagREBARINFO
title: REBARINFO (commctrl.h)
description: Contains information that describes rebar control characteristics.
helpviewer_keywords: ["*LPREBARINFO","LPREBARINFO","LPREBARINFO structure pointer [Windows Controls]","RBIM_IMAGELIST","REBARINFO","REBARINFO structure [Windows Controls]","_win32_REBARINFO","_win32_REBARINFO_cpp","commctrl/LPREBARINFO","commctrl/REBARINFO","controls.REBARINFO","controls._win32_REBARINFO"]
old-location: controls\REBARINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\rebar\structures\rebarinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPREBARINFO, LPREBARINFO, LPREBARINFO structure pointer [Windows Controls], RBIM_IMAGELIST, REBARINFO, REBARINFO structure [Windows Controls], _win32_REBARINFO, _win32_REBARINFO_cpp, commctrl/LPREBARINFO, commctrl/REBARINFO, controls.REBARINFO, controls._win32_REBARINFO'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: REBARINFO, *LPREBARINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagREBARINFO
 - commctrl/tagREBARINFO
 - LPREBARINFO
 - commctrl/LPREBARINFO
 - REBARINFO
 - commctrl/REBARINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - REBARINFO
---

# REBARINFO structure


## -description

Contains information that describes rebar control characteristics.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of this structure, in bytes. Your application must fill this member before sending any messages that use the address of this structure as a parameter.

### -field fMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flag values that describe characteristics of the rebar control. Currently, rebar controls support only one value: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RBIM_IMAGELIST"></a><a id="rbim_imagelist"></a><dl>
<dt><b>RBIM_IMAGELIST</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>himl</b> member is valid or must be filled. 

</td>
</tr>
</table>

### -field himl

Type: <b>HIMAGELIST</b>

Handle to an image list. The rebar control will use the specified image list to obtain images.