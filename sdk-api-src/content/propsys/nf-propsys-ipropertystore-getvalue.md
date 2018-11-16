---
UID: NF:propsys.IPropertyStore.GetValue
title: IPropertyStore::GetValue
author: windows-sdk-content
description: Gets data for a specific property.
old-location: properties\IPropertyStore_GetValue.htm
tech.root: properties
ms.assetid: 1768b087-1a80-4331-93b0-14eaab651913
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetValue, GetValue method [Windows Properties], GetValue method [Windows Properties],IPropertyStore interface, IPropertyStore interface [Windows Properties],GetValue method, IPropertyStore.GetValue, IPropertyStore::GetValue, properties.IPropertyStore_GetValue, propsys/IPropertyStore::GetValue, shell.IPropertyStore_GetValue, shell_IPropertyStore_GetValue
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
 - IPropertyStore.GetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- propsys.h
: 
- IPropertyStore.GetValue
: 
---

# IPropertyStore::GetValue


## -description


Gets data for a specific property.


## -parameters




### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to the <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structure retrieved through <a href="shell.IPropertyStore_GetAt">IPropertyStore::GetAt</a>. This structure contains a unique identifier for the property in question.


### -param pv [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this method returns, contains a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains the property data.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> or INPLACE_S_TRUNCATED if successful, or an error value otherwise.
                
                    

INPLACE_S_TRUNCATED is returned to indicate that the returned PROPVARIANT was coerced to a more canonical form, for instance to trim leading or trailing spaces from a string value. Most code should use the SUCCEEDED macro to check the return value, which treats INPLACE_S_TRUNCATED as a success code.




## -remarks



If the <a href="shell.PROPERTYKEY">PROPERTYKEY</a> referenced in <i>key</i> is not present in the property store, this method returns <b>S_OK</b> and the <b>vt</b> member of the structure pointed to by <i>pv</i> is set to VT_EMPTY.

File property handler implementers can use <a href="shell.IPropertyStore_GetValue">IPropertyStore::GetValue</a> to retrieve the property value by using the filestream with which <a href="https://msdn.microsoft.com/1e04c0a4-aa9b-4e2c-8307-525809ca903f">Initialize</a> initialized the property handler. The value can also be computed from an in-memory cache, or other means. However, most consumers of the property system obtain <a href="shell.IPropertyStore">IPropertyStore</a> through <a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">GetPropertyStore</a> and are not—and have no need to be—aware of the method of initialization.
            



