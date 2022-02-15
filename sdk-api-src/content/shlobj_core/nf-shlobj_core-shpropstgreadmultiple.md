---
UID: NF:shlobj_core.SHPropStgReadMultiple
title: SHPropStgReadMultiple function (shlobj_core.h)
description: Wraps the IPropertyStorage::ReadMultiple function to ensure that ANSI and Unicode translations are handled properly for deprecated property sets.
helpviewer_keywords: ["SHPropStgReadMultiple","SHPropStgReadMultiple function [Windows Properties]","_win32_SHPropStgReadMultiple","properties.SHPropStgReadMultiple","shell.SHPropStgReadMultiple","shlobj_core/SHPropStgReadMultiple"]
old-location: properties\SHPropStgReadMultiple.htm
tech.root: properties
ms.assetid: 5350a1b1-a099-4b09-af89-f652e40b1d20
ms.date: 12/05/2018
ms.keywords: SHPropStgReadMultiple, SHPropStgReadMultiple function [Windows Properties], _win32_SHPropStgReadMultiple, properties.SHPropStgReadMultiple, shell.SHPropStgReadMultiple, shlobj_core/SHPropStgReadMultiple
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHPropStgReadMultiple
 - shlobj_core/SHPropStgReadMultiple
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHPropStgReadMultiple
---

# SHPropStgReadMultiple function


## -description

<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Wraps the <a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-readmultiple">IPropertyStorage::ReadMultiple</a> function to ensure that ANSI and Unicode translations are handled properly for deprecated property sets.

## -parameters

### -param pps [in]

Type: <b><a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>*</b>

An <a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interface pointer that identifies the property store.

### -param uCodePage

Type: <b>UINT</b>

A code page value for ANSI string properties.

### -param cpspec

Type: <b>ULONG</b>

A count of properties being read.

### -param rgpspec [in]

Type: <b>PROPSPEC const[]</b>

An array of properties to be read.

### -param rgvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>[]</b>

An array of <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> types that, when this function returns successfully, receives the property values.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.