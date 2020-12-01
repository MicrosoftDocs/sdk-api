---
UID: NS:shtypes._SHITEMID
title: SHITEMID (shtypes.h)
description: Defines an item identifier.
helpviewer_keywords: ["*LPSHITEMID","SHITEMID","SHITEMID structure [Windows Shell]","_win32_SHITEMID","shell.SHITEMID","shtypes/SHITEMID"]
old-location: shell\SHITEMID.htm
tech.root: shell
ms.assetid: 794c8425-2319-4339-881c-c5083ab05638
ms.date: 12/05/2018
ms.keywords: '*LPSHITEMID, SHITEMID, SHITEMID structure [Windows Shell], _win32_SHITEMID, shell.SHITEMID, shtypes/SHITEMID'
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
targetos: Windows
req.typenames: SHITEMID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHITEMID
 - shtypes/_SHITEMID
 - SHITEMID
 - shtypes/SHITEMID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shtypes.h
api_name:
 - SHITEMID
---

# SHITEMID structure


## -description

Defines an item identifier.

## -struct-fields

### -field cb

Type: <b>USHORT</b>

The size of identifier, in bytes, including <b>cb</b> itself.

### -field abID

Type: <b>BYTE[1]</b>

A variable-length item identifier.

