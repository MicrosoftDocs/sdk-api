---
UID: NS:shlwapi.QITAB
title: QITAB (shlwapi.h)
description: Used by the QISearch function to describe a single interface.
helpviewer_keywords: ["*LPQITAB","LPQITAB","LPQITAB structure pointer [Windows Shell]","QITAB","QITAB structure [Windows Shell]","_win32_QITAB","shell.QITAB","shlwapi/LPQITAB","shlwapi/QITAB"]
old-location: shell\QITAB.htm
tech.root: shell
ms.assetid: 3a055773-6e53-45e1-8936-011a8b2b8b16
ms.date: 12/05/2018
ms.keywords: '*LPQITAB, LPQITAB, LPQITAB structure pointer [Windows Shell], QITAB, QITAB structure [Windows Shell], _win32_QITAB, shell.QITAB, shlwapi/LPQITAB, shlwapi/QITAB'
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
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
req.typenames: QITAB, *LPQITAB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPQITAB
 - shlwapi/LPQITAB
 - QITAB
 - shlwapi/QITAB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - QITAB
---

# QITAB structure


## -description

Used by the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-qisearch">QISearch</a> function to describe a single interface.

## -struct-fields

### -field piid

Type: <b>const IID*</b>

A pointer to the IID of the interface represented by this structure.

### -field dwOffset

Type: <b>int</b>

The offset, in bytes, from the base of the object to the start of the interface.

## -remarks

<div class="alert"><b>Note</b>  Prior to Windows Vista, <b>QITAB</b> was not declared in a public header file. To use it in those cases, you must use define it yourself as it is given here. Under Windows Vista, <b>QITAB</b> is included in Shlwapi.h and this is not necessary.</div>
<div> </div>
To mark the end of a <b>QITAB</b> table, set the <b>piid</b> member to <b>NULL</b> and the <b>dwOffset</b> member to 0. See the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-qisearch">QISearch</a> function for an example of how to use this structure.

