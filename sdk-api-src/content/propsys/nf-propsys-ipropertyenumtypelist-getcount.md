---
UID: NF:propsys.IPropertyEnumTypeList.GetCount
title: IPropertyEnumTypeList::GetCount
author: windows-sdk-content
description: Gets the number of elements in the list.
old-location: properties\IPropertyEnumTypeList_GetCount.htm
tech.root: properties
ms.assetid: 1ba42c48-afd2-4d96-8d9d-ebbe116807ca
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetCount, GetCount method [Windows Properties], GetCount method [Windows Properties],IPropertyEnumTypeList interface, IPropertyEnumTypeList interface [Windows Properties],GetCount method, IPropertyEnumTypeList.GetCount, IPropertyEnumTypeList::GetCount, _shell_IPropertyEnumTypeList_GetCount, properties.IPropertyEnumTypeList_GetCount, propsys/IPropertyEnumTypeList::GetCount, shell.IPropertyEnumTypeList_GetCount
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyEnumTypeList.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyEnumTypeList::GetCount


## -description


Gets the number of elements in the list.


## -parameters




### -param pctypes [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the number of list elements.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



