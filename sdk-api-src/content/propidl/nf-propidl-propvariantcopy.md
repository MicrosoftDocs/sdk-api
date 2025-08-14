---
UID: NF:propidl.PropVariantCopy
title: PropVariantCopy function (propidl.h)
description: Creates a copy of a PROPVARIANT structure.
helpviewer_keywords: ["PropVariantCopy","PropVariantCopy function [Windows Properties]","_shell_PropVariantCopy","properties.PropVariantCopy","propidl/PropVariantCopy","shell.PropVariantCopy"]
old-location: properties\PropVariantCopy.htm
tech.root: properties
ms.assetid: f17f1722-f041-414c-b838-f1f83427ff0c
ms.date: 12/05/2018
ms.keywords: PropVariantCopy, PropVariantCopy function [Windows Properties], _shell_PropVariantCopy, properties.PropVariantCopy, propidl/PropVariantCopy, shell.PropVariantCopy
req.header: propidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PropVariantCopy
 - propidl/PropVariantCopy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - PropVariantCopy
---

# PropVariantCopy function


## -description

Creates a copy of a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -parameters

### -param pvarDest [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer to the destination <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that receives the copy.

### -param pvarSrc [in]

Type: <b>const <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer to the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.