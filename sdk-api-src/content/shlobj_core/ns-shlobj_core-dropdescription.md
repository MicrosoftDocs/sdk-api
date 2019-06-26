---
UID: NS:shlobj_core.__unnamed_struct_8
title: DROPDESCRIPTION (shlobj_core.h)
author: windows-sdk-content
description: Describes the image and accompanying text for a drop object.
old-location: shell\DROPDESCRIPTION.htm
tech.root: shell
ms.assetid: 78757001-cac8-412d-a6c3-74bae6eb3ad8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DROPDESCRIPTION, DROPDESCRIPTION structure [Windows Shell], _shell_DROPDESCRIPTION, shell.DROPDESCRIPTION, shlobj_core/DROPDESCRIPTION
ms.topic: struct
f1_keywords: 
 - "shlobj_core/DROPDESCRIPTION"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - DROPDESCRIPTION
product: Windows
targetos: Windows
req.typenames: DROPDESCRIPTION
req.redist: 
ms.custom: 19H1
---

# DROPDESCRIPTION structure


## -description


Describes the image and accompanying text for a drop object.


## -struct-fields




### -field type

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype">DROPIMAGETYPE</a></b>

A <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype">DROPIMAGETYPE</a> indicating the stock image to use.


### -field szMessage

Type: <b>WCHAR[MAX_PATH]</b>

Text such as "Move to %1".


### -field szInsert

Type: <b>WCHAR[MAX_PATH]</b>

Text such as "Documents", inserted as specified by <b>szMessage</b>.


## -remarks



Some UI coloring is applied to the text in <b>szInsert</b> if used by specifying %1 in <b>szMessage</b>. The characters %% and %1 are the subset of <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> markers that are processed here.



