---
UID: NS:ocidl.tagCONTROLINFO
title: CONTROLINFO (ocidl.h)
description: Contains parameters that describe a control's keyboard mnemonics and keyboard behavior. The structure is populated during the IOleControl::GetControlInfo method.
helpviewer_keywords: ["*LPCONTROLINFO","CONTROLINFO","CONTROLINFO structure [COM]","LPCONTROLINFO","LPCONTROLINFO structure pointer [COM]","_ctrl_CONTROLINFO","com.controlinfo","ocidl/CONTROLINFO","ocidl/LPCONTROLINFO"]
old-location: com\controlinfo.htm
tech.root: com
ms.assetid: 3f22dc1d-554a-4dd1-a79a-121117f65caf
ms.date: 12/05/2018
ms.keywords: '*LPCONTROLINFO, CONTROLINFO, CONTROLINFO structure [COM], LPCONTROLINFO, LPCONTROLINFO structure pointer [COM], _ctrl_CONTROLINFO, com.controlinfo, ocidl/CONTROLINFO, ocidl/LPCONTROLINFO'
req.header: ocidl.h
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
req.typenames: CONTROLINFO, *LPCONTROLINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCONTROLINFO
 - ocidl/tagCONTROLINFO
 - LPCONTROLINFO
 - ocidl/LPCONTROLINFO
 - CONTROLINFO
 - ocidl/CONTROLINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - CONTROLINFO
---

# CONTROLINFO structure


## -description

Contains parameters that describe a control's keyboard mnemonics and keyboard behavior. The structure is populated during the <a href="/windows/desktop/api/ocidl/nf-ocidl-iolecontrol-getcontrolinfo">IOleControl::GetControlInfo</a> method.

## -struct-fields

### -field cb

The size of the structure, in bytes.

### -field hAccel

A handle to an array of <a href="/windows/desktop/api/winuser/ns-winuser-accel">ACCEL</a> structures, each structure describing a keyboard mnemonic. The array is created with the <a href="/windows/desktop/api/winuser/nf-winuser-createacceleratortablea">CreateAcceleratorTable</a> function. The control always maintains the memory for this array; the caller of <a href="/windows/desktop/api/ocidl/nf-ocidl-iolecontrol-getcontrolinfo">IOleControl::GetControlInfo</a> should not attempt to free the memory.

### -field cAccel

The number of mnemonics described in the <b>hAccel</b> field. This value can be zero to indicate no mnemonics.

### -field dwFlags

Flags that indicate the keyboard behavior of the control. The possible values are:

<ul>
<li>CTRLINFO_EATS_RETURN: When the control has the focus, it will process the Return key. 
</li>
<li>CTRLINFO_EATS_ESCAPE: When the control has the focus, it will process the Escape key. </li>
</ul>
When the control has the focus, the dialog box containing the control cannot use the Return or Escape keys as mnemonics for the default and cancel buttons.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-iolecontrol-getcontrolinfo">IOleControl::GetControlInfo</a>