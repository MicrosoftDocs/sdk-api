---
UID: NF:comadmin.ICatalogObject.IsPropertyReadOnly
title: ICatalogObject::IsPropertyReadOnly
author: windows-driver-content
description: Indicates whether the specified property can be modified using Value.
old-location: cos\icatalogobject_ispropertyreadonly.htm
old-project: cossdk
ms.assetid: bd088794-1245-4cb8-a1f7-385354640675
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ICatalogObject interface [COM+],IsPropertyReadOnly method, ICatalogObject.IsPropertyReadOnly, ICatalogObject::IsPropertyReadOnly, IsPropertyReadOnly, IsPropertyReadOnly method [COM+], IsPropertyReadOnly method [COM+],ICatalogObject interface, _cos_ICatalogObject_IsPropertyReadOnly, comadmin/ICatalogObject::IsPropertyReadOnly, cos.icatalogobject_ispropertyreadonly
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
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComAdmin.h
api_name:
-	ICatalogObject.IsPropertyReadOnly
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICatalogObject::IsPropertyReadOnly


## -description


Indicates whether the specified property can be modified using <a href="https://msdn.microsoft.com/library/windows/hardware/dn923306">Value</a>.


## -parameters




### -param bstrPropName [in]

The name of the property to be modified.


### -param pbRetVal [out, retval]

If this value is True, you cannot modify the property. Otherwise, you can modify the property.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/fe3f7452-57b2-4f9e-9b48-5dedfe519ac1">ICatalogObject</a>
 

 

