---
UID: NE:shlobj_core.DROPIMAGETYPE
title: DROPIMAGETYPE
author: windows-sdk-content
description: Values used with the DROPDESCRIPTION structure to specify the drop image.
old-location: shell\DROPIMAGETYPE.htm
tech.root: shell
ms.assetid: eeaf8bd4-25ab-4ec3-9da9-9a72ba3813b9
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: DROPIMAGETYPE, DROPIMAGETYPE enumeration [Windows Shell], DROPIMAGE_COPY, DROPIMAGE_INVALID, DROPIMAGE_LABEL, DROPIMAGE_LINK, DROPIMAGE_MOVE, DROPIMAGE_NOIMAGE, DROPIMAGE_NONE, DROPIMAGE_WARNING, _shell_DROPIMAGETYPE, shell.DROPIMAGETYPE, shlobj_core/DROPIMAGETYPE, shlobj_core/DROPIMAGE_COPY, shlobj_core/DROPIMAGE_INVALID, shlobj_core/DROPIMAGE_LABEL, shlobj_core/DROPIMAGE_LINK, shlobj_core/DROPIMAGE_MOVE, shlobj_core/DROPIMAGE_NOIMAGE, shlobj_core/DROPIMAGE_NONE, shlobj_core/DROPIMAGE_WARNING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - DROPIMAGETYPE
product: Windows
targetos: Windows
req.typenames: DROPIMAGETYPE
req.redist: 
---

# DROPIMAGETYPE enumeration


## -description


Values used with the <a href="https://msdn.microsoft.com/78757001-cac8-412d-a6c3-74bae6eb3ad8">DROPDESCRIPTION</a> structure to specify the drop image.


## -enum-fields




### -field DROPIMAGE_INVALID

No drop image preference; use the default image.


### -field DROPIMAGE_NONE

A red bisected circle such as that found on a "no smoking" sign.


### -field DROPIMAGE_COPY

A plus sign (+) that indicates a copy operation.


### -field DROPIMAGE_MOVE

An arrow that indicates a move operation.


### -field DROPIMAGE_LINK

An arrow that indicates a link.


### -field DROPIMAGE_LABEL

A tag icon that indicates that the metadata will be changed.


### -field DROPIMAGE_WARNING

A yellow exclamation mark that indicates that a problem has been encountered in the operation.


### -field DROPIMAGE_NOIMAGE

<b>Windows 7 and later</b>. Use no drop image.

