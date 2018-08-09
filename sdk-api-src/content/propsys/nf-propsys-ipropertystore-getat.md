---
UID: NF:propsys.IPropertyStore.GetAt
title: IPropertyStore::GetAt
author: windows-sdk-content
description: Gets a property key from the property array of an item.
old-location: audio\ipropertystore_getat.htm
old-project: audio
ms.assetid: 4f93949a-d5d5-4fbf-8538-6171861e5884
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetAt, GetAt (IPropertyStore), GetAt method [Audio Devices], GetAt method [Audio Devices],IPropertyStore interface, IPropertyStore interface [Audio Devices],GetAt method, IPropertyStore.GetAt, IPropertyStore::GetAt, audio.ipropertystore_getat, audio_syseffects_r_3a52a0be-2e51-468f-9a93-86bd242b422e.xml, propsys/IPropertyStore::GetAt
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
 - IPropertyStore.GetAt
product: Windows
targetos: Windows
req.lib: Propsys.idl
req.dll: 
req.irql: All levels
req.product: ADAM
---

# IPropertyStore::GetAt


## -description


Gets a property key from the property array of an item.


## -parameters




### -param iProp

The index of the property key in the array of PROPERTYKEY structures. This is a zero-based index.


### -param pkey






#### - pKey

A pointer to a PROPERTYKEY structure and it can be used in subsequent calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536962">IPropertyStore::GetValue</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff536963">IPropertyStore::SetValue</a>.


## -returns



The <code>IPropertyStore::GetAt</code> method returns a value of S_OK if successful. Otherwise, any other code it returns must be considered to be an error code.




## -remarks



None




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536962">IPropertyStore::GetValue</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536963">IPropertyStore::SetValue</a>
 

 

