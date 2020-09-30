---
UID: NS:richedit._enlowfirtf
title: ENLOWFIRTF (richedit.h)
description: Contains information about an unsupported Rich Text Format (RTF) keyword in a Microsoft Rich Edit control.
helpviewer_keywords: ["ENLOWFIRTF","ENLOWFIRTF structure [Windows Controls]","_win32_ENLOWFIRTF_str","_win32_ENLOWFIRTF_str_cpp","controls.ENLOWFIRTF","controls._win32_ENLOWFIRTF_str","richedit/ENLOWFIRTF"]
old-location: controls\ENLOWFIRTF.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\enlowfirtf.htm
ms.date: 12/05/2018
ms.keywords: ENLOWFIRTF, ENLOWFIRTF structure [Windows Controls], _win32_ENLOWFIRTF_str, _win32_ENLOWFIRTF_str_cpp, controls.ENLOWFIRTF, controls._win32_ENLOWFIRTF_str, richedit/ENLOWFIRTF
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.typenames: ENLOWFIRTF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _enlowfirtf
 - richedit/_enlowfirtf
 - ENLOWFIRTF
 - richedit/ENLOWFIRTF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - ENLOWFIRTF
---

# ENLOWFIRTF structure


## -description

Contains information about an unsupported Rich Text Format (RTF) keyword in a Microsoft Rich Edit control.

## -struct-fields

### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

Specifies an <a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure.

### -field szControl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">CHAR</a>*</b>

The unsupported RTF keyword.

## -remarks

This structure is used with the <a href="https://msdn.microsoft.com/3b18320b-ebc3-44f2-a93c-e967a028c522">EN_LOWFIRTF</a> message.

## -see-also

<a href="https://msdn.microsoft.com/3b18320b-ebc3-44f2-a93c-e967a028c522">EN_LOWFIRTF</a>