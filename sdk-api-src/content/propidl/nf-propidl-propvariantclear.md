---
UID: NF:propidl.PropVariantClear
title: PropVariantClear function (propidl.h)
description: Clears a PROPVARIANT structure.
old-location: properties\PropVariantClear.htm
tech.root: properties
ms.assetid: 68b00e4b-39d3-49e3-8a0d-032edcb23b06
ms.date: 12/05/2018
ms.keywords: PropVariantClear, PropVariantClear function [Windows Properties], _shell_PropVariantClear, properties.PropVariantClear, propidl/PropVariantClear, shell.PropVariantClear
f1_keywords:
- propidl/PropVariantClear
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ole32.dll
- API-MS-Win-Core-Com-l1-1-0.dll
- ComBase.dll
- API-MS-Win-Core-Com-l1-1-1.dll
- API-MS-Win-DownLevel-Ole32-l1-1-0.dll
- API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
- PropVariantClear
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# PropVariantClear function


## -description


Clears a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.


## -parameters




### -param pvar [in, out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure to clear. When this function successfully returns, the <b>PROPVARIANT</b> is zeroed and the type is set to VT_EMPTY.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



