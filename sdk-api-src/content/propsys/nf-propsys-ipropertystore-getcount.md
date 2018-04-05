---
UID: NF:propsys.IPropertyStore.GetCount
title: IPropertyStore::GetCount method
author: windows-driver-content
description: Gets the number of properties attached to the file.
old-location: properties\IPropertyStore_GetCount.htm
old-project: properties
ms.assetid: d7e125ef-01f0-410b-a24b-6e86c1df25c5
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetCount method [Windows Properties], GetCount method [Windows Properties], IPropertyStore interface, GetCount,IPropertyStore.GetCount, IPropertyStore, IPropertyStore interface [Windows Properties], GetCount method, IPropertyStore::GetCount, properties.IPropertyStore_GetCount, propsys/IPropertyStore::GetCount, shell.IPropertyStore_GetCount, shell_IPropertyStore_GetCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
-	IPropertyStore.GetCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPropertyStore::GetCount method


## -description


Gets the number of properties attached to the file.


## -parameters




### -param cProps [out]

Type: <b>DWORD*</b>

When this method returns, contains the property count.


## -returns



Type: <b>HRESULT</b>


<a href="https://msdn.microsoft.com/library/windows/hardware/ff536960">IPropertyStore::GetCount</a> returns <b>S_OK</b> on success, even if the file has no properties.




## -remarks



IPropertyStore provides an abstraction over an array of property keys via the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536960">IPropertyStore::GetCount</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a> methods. The property keys in this array represent the properties currently stored by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>.

When GetCount succeeds, the value pointed to by pcProps is a count of property keys in the array. The caller can expect calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a> to succeed for values of <i>iProp</i> less than <i>pcProps</i>.

<b>Calling applicatons:</b> GetCount and GetAt may not return the full set of properties that are supported by a particular property store.  In some cases, the property store is capable of storing any property key, and thus only enumerates the keys already in the store.  Some callers may find property lists useful for determining a list of properties that users find useful for a particular file type.

<b>Implementers:</b> In the case of failures such as E_OUTOFMEMORY, you should set <i>cProps</i> to zero.  It is preferable that errors are discovered during creation or initialization of the property store.



