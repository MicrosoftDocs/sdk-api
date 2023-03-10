---
UID: NF:shlobj_core.SHPropStgWriteMultiple
title: SHPropStgWriteMultiple function (shlobj_core.h)
description: Wraps the IPropertyStorage::WriteMultiple function to ensure that ANSI and Unicode translations are handled properly for deprecated property sets.
helpviewer_keywords: ["SHPropStgWriteMultiple","SHPropStgWriteMultiple function [Windows Properties]","_win32_SHPropStgWriteMultiple","properties.SHPropStgWriteMultiple","shell.SHPropStgWriteMultiple","shlobj_core/SHPropStgWriteMultiple"]
old-location: properties\SHPropStgWriteMultiple.htm
tech.root: properties
ms.assetid: 38bc4d53-818d-48c5-9ec5-d2e33d98c63e
ms.date: 12/05/2018
ms.keywords: SHPropStgWriteMultiple, SHPropStgWriteMultiple function [Windows Properties], _win32_SHPropStgWriteMultiple, properties.SHPropStgWriteMultiple, shell.SHPropStgWriteMultiple, shlobj_core/SHPropStgWriteMultiple
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
 - SHPropStgWriteMultiple
 - shlobj_core/SHPropStgWriteMultiple
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
 - SHPropStgWriteMultiple
---

# SHPropStgWriteMultiple function


## -description

<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Wraps the <a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writemultiple">IPropertyStorage::WriteMultiple</a> function to ensure that ANSI and Unicode translations are handled properly for deprecated property sets.

## -parameters

### -param pps [in]

Type: <b><a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>*</b>

An <a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interface pointer that identifies the property store.

### -param puCodePage [in, out, optional]

Type: <b>UINT*</b>

A pointer to the code page value for ANSI string properties.

### -param cpspec

Type: <b>ULONG</b>

A count of properties being set.

### -param rgpspec [in]

Type: <b>PROPSPEC const[]</b>

An array of PROPSPEC structures that contain the property information to be set.

### -param rgvar [in, out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>[]</b>

An array of <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> types to set the property values.

### -param propidNameFirst

Type: <b>PROPID</b>

The minimum value for property identifiers when they must be allocated. The value should be greater than or equal to PID_FIRST_USABLE.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.