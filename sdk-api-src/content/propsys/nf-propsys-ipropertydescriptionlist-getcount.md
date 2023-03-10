---
UID: NF:propsys.IPropertyDescriptionList.GetCount
title: IPropertyDescriptionList::GetCount (propsys.h)
description: Gets the number of properties included in the property list.
helpviewer_keywords: ["GetCount","GetCount method [Windows Properties]","GetCount method [Windows Properties]","IPropertyDescriptionList interface","IPropertyDescriptionList interface [Windows Properties]","GetCount method","IPropertyDescriptionList.GetCount","IPropertyDescriptionList::GetCount","_shell_IPropertyDescriptionList_GetCount","properties.IPropertyDescriptionList_GetCount","propsys/IPropertyDescriptionList::GetCount","shell.IPropertyDescriptionList_GetCount"]
old-location: properties\IPropertyDescriptionList_GetCount.htm
tech.root: properties
ms.assetid: 17d8b018-1709-42a7-9edf-e1c2886593de
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Windows Properties], GetCount method [Windows Properties],IPropertyDescriptionList interface, IPropertyDescriptionList interface [Windows Properties],GetCount method, IPropertyDescriptionList.GetCount, IPropertyDescriptionList::GetCount, _shell_IPropertyDescriptionList_GetCount, properties.IPropertyDescriptionList_GetCount, propsys/IPropertyDescriptionList::GetCount, shell.IPropertyDescriptionList_GetCount
req.header: propsys.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyDescriptionList::GetCount
 - propsys/IPropertyDescriptionList::GetCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - propsys.h
api_name:
 - IPropertyDescriptionList.GetCount
---

# IPropertyDescriptionList::GetCount


## -description

Gets the number of properties included in the property list.

## -parameters

### -param pcElem [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the count of properties.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

