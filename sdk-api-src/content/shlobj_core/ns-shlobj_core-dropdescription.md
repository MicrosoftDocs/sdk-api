---
UID: NS:shlobj_core.DROPDESCRIPTION
title: DROPDESCRIPTION
author: windows-driver-content
description: Describes the image and accompanying text for a drop object.
old-location: shell\DROPDESCRIPTION.htm
old-project: shell
ms.assetid: 78757001-cac8-412d-a6c3-74bae6eb3ad8
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: DROPDESCRIPTION, DROPDESCRIPTION structure [Windows Shell], _shell_DROPDESCRIPTION, shell.DROPDESCRIPTION, shlobj_core/DROPDESCRIPTION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: DROPDESCRIPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	shlobj_core.h
api_name:
-	DROPDESCRIPTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# DROPDESCRIPTION structure


## -description


Describes the image and accompanying text for a drop object.


## -struct-fields




### -field type

Type: <b><a href="https://msdn.microsoft.com/eeaf8bd4-25ab-4ec3-9da9-9a72ba3813b9">DROPIMAGETYPE</a></b>

A <a href="https://msdn.microsoft.com/eeaf8bd4-25ab-4ec3-9da9-9a72ba3813b9">DROPIMAGETYPE</a> indicating the stock image to use.


### -field szMessage

Type: <b>WCHAR[MAX_PATH]</b>

Text such as "Move to %1".


### -field szInsert

Type: <b>WCHAR[MAX_PATH]</b>

Text such as "Documents", inserted as specified by <b>szMessage</b>.


## -remarks



Some UI coloring is applied to the text in <b>szInsert</b> if used by specifying %1 in <b>szMessage</b>. The characters %% and %1 are the subset of <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> markers that are processed here.



