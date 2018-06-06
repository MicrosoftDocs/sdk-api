---
UID: NF:shlobj_core.SHPropStgReadMultiple
title: SHPropStgReadMultiple function
author: windows-sdk-content
description: Wraps the IPropertyStorage::ReadMultiple function to ensure that ANSI and Unicode translations are handled properly for deprecated property sets.
old-location: properties\SHPropStgReadMultiple.htm
old-project: properties
ms.assetid: 5350a1b1-a099-4b09-af89-f652e40b1d20
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: SHPropStgReadMultiple, SHPropStgReadMultiple function [Windows Properties], _win32_SHPropStgReadMultiple, properties.SHPropStgReadMultiple, shell.SHPropStgReadMultiple, shlobj_core/SHPropStgReadMultiple
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHPropStgReadMultiple
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHPropStgReadMultiple function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Wraps the <a href="https://msdn.microsoft.com/a3d708fe-53af-4f1b-94ac-edc40d59a034">IPropertyStorage::ReadMultiple</a> function to ensure that ANSI and Unicode translations are handled properly for deprecated property sets.


## -parameters




### -param pps [in]

Type: <b><a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>*</b>

An <a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface pointer that identifies the property store.


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

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>[]</b>

An array of <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> types that, when this function returns successfully, receives the property values.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



