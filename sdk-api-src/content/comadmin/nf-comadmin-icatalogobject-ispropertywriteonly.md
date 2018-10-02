---
UID: NF:comadmin.ICatalogObject.IsPropertyWriteOnly
title: ICatalogObject::IsPropertyWriteOnly
author: windows-sdk-content
description: Indicates whether the specified property can be read using Value.
old-location: cos\icatalogobject_ispropertywriteonly.htm
tech.root: cossdk
ms.assetid: 463ca1eb-5386-4265-882b-fa29c4cbe877
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICatalogObject interface [COM+],IsPropertyWriteOnly method, ICatalogObject.IsPropertyWriteOnly, ICatalogObject::IsPropertyWriteOnly, IsPropertyWriteOnly, IsPropertyWriteOnly method [COM+], IsPropertyWriteOnly method [COM+],ICatalogObject interface, _cos_ICatalogObject_IsPropertyWriteOnly, comadmin/ICatalogObject::IsPropertyWriteOnly, cos.icatalogobject_ispropertywriteonly
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
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
 - ComAdmin.h
api_name:
 - ICatalogObject.IsPropertyWriteOnly
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICatalogObject::IsPropertyWriteOnly


## -description


Indicates whether the specified property can be read using <a href="https://msdn.microsoft.com/en-us/library/ms687686(v=VS.85).aspx">Value</a>.


## -parameters




### -param bstrPropName [in]

The name of the property to be read.


### -param pbRetVal [out, retval]

If this value is True, you cannot read the property. Otherwise, you can read the property.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms688526(v=VS.85).aspx">ICatalogObject</a>
 

 

