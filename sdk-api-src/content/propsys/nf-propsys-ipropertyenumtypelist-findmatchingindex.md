---
UID: NF:propsys.IPropertyEnumTypeList.FindMatchingIndex
title: IPropertyEnumTypeList::FindMatchingIndex
author: windows-driver-content
description: Compares the specified property value against the enumerated values in a list and returns the matching index.
old-location: properties\IPropertyEnumTypeList_FindMatchingIndex.htm
old-project: properties
ms.assetid: 48f2d55e-d801-4518-b587-7818cd6afcc9
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: FindMatchingIndex, FindMatchingIndex method [Windows Properties], FindMatchingIndex method [Windows Properties],IPropertyEnumTypeList interface, IPropertyEnumTypeList interface [Windows Properties],FindMatchingIndex method, IPropertyEnumTypeList.FindMatchingIndex, IPropertyEnumTypeList::FindMatchingIndex, _shell_IPropertyEnumTypeList_FindMatchingIndex, properties.IPropertyEnumTypeList_FindMatchingIndex, propsys/IPropertyEnumTypeList::FindMatchingIndex, shell.IPropertyEnumTypeList_FindMatchingIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyEnumTypeList.FindMatchingIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyEnumTypeList::FindMatchingIndex


## -description


Compares the specified property value against the enumerated values in a list and returns the matching index.


## -parameters




### -param propvarCmp [in]

Type: <b>REFPROPVARIANT</b>

A reference to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that represents the property value.


### -param pnIndex [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the index in the enumerated type list that matches the property value, if any.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



