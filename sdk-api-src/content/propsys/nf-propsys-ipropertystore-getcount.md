---
UID: NF:propsys.IPropertyStore.GetCount
title: IPropertyStore::GetCount
author: windows-sdk-content
description: This method returns a count of the number of properties that are attached to the file.
old-location: audio\ipropertystore_getcount.htm
old-project: audio
ms.assetid: 23f7b982-29db-4960-9a1d-2f9e033ebf61
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: GetCount, GetCount (IPropertyStore), GetCount method [Audio Devices], GetCount method [Audio Devices],IPropertyStore interface, IPropertyStore interface [Audio Devices],GetCount method, IPropertyStore.GetCount, IPropertyStore::GetCount, audio.ipropertystore_getcount, audio_syseffects_r_2670eef9-2f2a-4e3d-8a43-d8d61a9ebce5.xml, propsys/IPropertyStore::GetCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available with Windows Vista and later versions of the Windows operating system.
req.target-min-winversvr: 
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
req.typenames: PSC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.idl
 - Propsys.idl.dll
api_name:
 - IPropertyStore.GetCount
product: Windows
targetos: Windows
req.lib: Propsys.idl
req.dll: 
req.irql: All levels
req.product: Rights Management Services client 1.0 or later
---

# IPropertyStore::GetCount


## -description


This method returns a count of the number of properties that are attached to the file.


## -parameters




### -param cProps

A pointer to a value that indicates the property count.


## -returns



The <code>IpropertyStore::GetCount</code> method returns a value of S_OK when the call is successful, even if the file has no properties attached. Any other code returned is an error code.




## -remarks



<b>IPropertyStore</b> provides an abstraction over an array of property keys via the <code>IPropertyStore::GetCount</code> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a> methods. The property keys in this array represent the properties that are currently stored by the <b>IPropertyStore</b>.

When <code>GetCount</code> succeeds, the value pointed to by cProps is a count of property keys in the array. The caller can expect calls to <b>IPropertyStore::GetAt</b> to succeed for values of iProp less than cProps.

In the case of failures such as E_OUTOFMEMORY, you should set cProps to zero. It is preferable that errors are discovered during creation or initialization of the property store.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a>
 

 

