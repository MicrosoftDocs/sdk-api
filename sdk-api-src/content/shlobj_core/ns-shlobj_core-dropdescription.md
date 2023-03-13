---
UID: NS:shlobj_core.DROPDESCRIPTION
title: DROPDESCRIPTION (shlobj_core.h)
description: Describes the image and accompanying text for a drop object.
helpviewer_keywords: ["DROPDESCRIPTION","DROPDESCRIPTION structure [Windows Shell]","_shell_DROPDESCRIPTION","shell.DROPDESCRIPTION","shlobj_core/DROPDESCRIPTION"]
old-location: shell\DROPDESCRIPTION.htm
tech.root: shell
ms.assetid: 78757001-cac8-412d-a6c3-74bae6eb3ad8
ms.date: 12/05/2018
ms.keywords: DROPDESCRIPTION, DROPDESCRIPTION structure [Windows Shell], _shell_DROPDESCRIPTION, shell.DROPDESCRIPTION, shlobj_core/DROPDESCRIPTION
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: DROPDESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DROPDESCRIPTION
 - shlobj_core/DROPDESCRIPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - DROPDESCRIPTION
---

# DROPDESCRIPTION structure


## -description

Describes the image and accompanying text for a drop object.

## -struct-fields

### -field type

Type: <b><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype">DROPIMAGETYPE</a></b>

A <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype">DROPIMAGETYPE</a> indicating the stock image to use.

### -field szMessage

Type: <b>WCHAR[MAX_PATH]</b>

Text such as "Move to %1".

### -field szInsert

Type: <b>WCHAR[MAX_PATH]</b>

Text such as "Documents", inserted as specified by <b>szMessage</b>.

## -remarks

Some UI coloring is applied to the text in <b>szInsert</b> if used by specifying %1 in <b>szMessage</b>. The characters %% and %1 are the subset of <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> markers that are processed here.

