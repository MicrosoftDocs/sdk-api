---
UID: NF:propsys.INamedPropertyStore.GetNamedValue
title: INamedPropertyStore::GetNamedValue
author: windows-sdk-content
description: Gets the value of a named property from the named property store.
old-location: shell\INamedPropertyStore_GetNamedValue.htm
tech.root: shell
ms.assetid: d62fcacd-7af5-4618-9b76-bebb001bb827
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetNamedValue, GetNamedValue method [Windows Shell], GetNamedValue method [Windows Shell],INamedPropertyStore interface, INamedPropertyStore interface [Windows Shell],GetNamedValue method, INamedPropertyStore.GetNamedValue, INamedPropertyStore::GetNamedValue, _shell_INamedPropertyStore_GetNamedValue, propsys/INamedPropertyStore::GetNamedValue, shell.INamedPropertyStore_GetNamedValue
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
 - INamedPropertyStore.GetNamedValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INamedPropertyStore::GetNamedValue


## -description


Gets the value of a named property from the named property store.


## -parameters




### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to the property name, as a Unicode string, of the property in the named property store.


### -param ppropvar

TBD




#### - pv [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this method returns, contains a pointer to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that holds the property's value.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.
                
                    

If the property named in <i>pszName</i> is not found in the property store, this method returns S_OK and the <i>pv</i> member is set to VT_EMPTY.



