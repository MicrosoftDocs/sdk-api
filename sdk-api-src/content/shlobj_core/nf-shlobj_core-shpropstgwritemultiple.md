---
UID: NF:shlobj_core.SHPropStgWriteMultiple
title: SHPropStgWriteMultiple function
author: windows-driver-content
description: Wraps the IPropertyStorage::WriteMultiple function to ensure that ANSI and Unicode translations are handled properly for deprecated property sets.
old-location: properties\SHPropStgWriteMultiple.htm
old-project: properties
ms.assetid: 38bc4d53-818d-48c5-9ec5-d2e33d98c63e
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: SHPropStgWriteMultiple, SHPropStgWriteMultiple function [Windows Properties], _win32_SHPropStgWriteMultiple, properties.SHPropStgWriteMultiple, shell.SHPropStgWriteMultiple, shlobj_core/SHPropStgWriteMultiple
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
api_name:
-	SHPropStgWriteMultiple
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHPropStgWriteMultiple function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Wraps the <a href="https://msdn.microsoft.com/480a2be3-ccb0-4135-a085-733f6ab48ccd">IPropertyStorage::WriteMultiple</a> function to ensure that ANSI and Unicode translations are handled properly for deprecated property sets.


## -parameters




### -param pps [in]

Type: <b><a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>*</b>

An <a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface pointer that identifies the property store.


### -param puCodePage

TBD


### -param cpspec

Type: <b>ULONG</b>

A count of properties being set.


### -param rgpspec [in]

Type: <b>PROPSPEC const[]</b>

An array of PROPSPEC structures that contain the property information to be set.


### -param rgvar [in, out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>[]</b>

An array of <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> types to set the property values.


### -param propidNameFirst

Type: <b>PROPID</b>

The minimum value for property identifiers when they must be allocated. The value should be greater than or equal to PID_FIRST_USABLE.


#### - uCodePage [in, out, optional]

Type: <b>UINT*</b>

A pointer to the code page value for ANSI string properties.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



