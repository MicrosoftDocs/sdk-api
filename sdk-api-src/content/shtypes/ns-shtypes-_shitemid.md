---
UID: NS:shtypes._SHITEMID
title: "_SHITEMID"
author: windows-sdk-content
description: Defines an item identifier.
old-location: shell\SHITEMID.htm
tech.root: shell
ms.assetid: 794c8425-2319-4339-881c-c5083ab05638
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*LPSHITEMID, SHITEMID, SHITEMID structure [Windows Shell], _SHITEMID, _win32_SHITEMID, shell.SHITEMID, shtypes/SHITEMID"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: shtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shtypes.idl
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
 - Shtypes.h
api_name:
 - SHITEMID
product: Windows
targetos: Windows
req.typenames: SHITEMID
req.redist: 
---

# _SHITEMID structure


## -description


Defines an item identifier.


## -struct-fields




### -field cb

Type: <b>USHORT</b>

The size of identifier, in bytes, including <b>cb</b> itself.


### -field abID

Type: <b>BYTE[1]</b>

A variable-length item identifier.

