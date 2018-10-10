---
UID: NF:propsys.IPropertyStore.GetAt
title: IPropertyStore::GetAt
author: windows-sdk-content
description: Gets a property key from an item's array of properties.
old-location: properties\IPropertyStore_GetAt.htm
tech.root: properties
ms.assetid: 7bf18e8b-f84a-44a3-bfee-971fed425823
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetAt, GetAt method [Windows Properties], GetAt method [Windows Properties],IPropertyStore interface, IPropertyStore interface [Windows Properties],GetAt method, IPropertyStore.GetAt, IPropertyStore::GetAt, properties.IPropertyStore_GetAt, propsys/IPropertyStore::GetAt, shell.IPropertyStore_GetAt, shell_IPropertyStore_GetAt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IPropertyStore.GetAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyStore::GetAt


## -description


Gets a property key from an item's array of properties.


## -parameters




### -param iProp [in]

Type: <b>DWORD</b>

The index of the property key in the array of <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structures. This is a zero-based index.


### -param pkey [out]

Type: <b><a href="shell.PROPERTYKEY">PROPERTYKEY</a>*</b>

When this method returns, contains a <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structure that receives the unique identifier for a property.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="shell.PROPERTYKEY">PROPERTYKEY</a> returned in <i>pkey</i> can be used in subsequent calls to <a href="shell.IPropertyStore_GetValue">IPropertyStore::GetValue</a> and <a href="shell.IPropertyStore_SetValue">IPropertyStore::SetValue</a>.

There is no specific order to an item's set of enumerated properties. To find a specific property, you must walk the array until you find the property that matches your criteria.

<i>iProp</i> cannot be greater than or equal to the <i>cProps</i> parameter retrieved by <a href="shell.IPropertyStore_GetCount">IPropertyStore::GetCount</a>. If it is greater than or equal to that value, <a href="shell.IPropertyStore_GetAt">IPropertyStore::GetAt</a> returns E_INVALIDARG and <i>pkey</i> is set to <b>NULL</b> by the property handler.



