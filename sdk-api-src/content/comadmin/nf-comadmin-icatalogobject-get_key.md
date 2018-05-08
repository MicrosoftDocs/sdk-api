---
UID: NF:comadmin.ICatalogObject.get_Key
title: ICatalogObject::get_Key
author: windows-driver-content
description: Retrieves the key property of the object.
old-location: cos\icatalogobject_key.htm
old-project: cossdk
ms.assetid: 1937cd5a-742f-4248-a4c2-0b39a03eed20
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: ICatalogObject interface [COM+],Key property, ICatalogObject.Key, ICatalogObject.get_Key, ICatalogObject::Key, ICatalogObject::get_Key, Key property [COM+], Key property [COM+],ICatalogObject interface, _cos_ICatalogObject_get_Key, comadmin/ICatalogObject::Key, comadmin/ICatalogObject::get_Key, cos.icatalogobject_key, get_Key
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
-	ICatalogObject.Key
-	ICatalogObject.get_Key
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICatalogObject::get_Key


## -description


Retrieves the key property of the object.

This property is read-only.


## -parameters


## -remarks



The key property serves as the primary identifier for a collection. In some cases, it is a GUID, such as CLSID for a component; in some cases, it is the object name, as with roles. The key property of a collection is identified in the documentation for each specific collection of the <a href="https://msdn.microsoft.com/eed8ca97-39ad-4188-afc6-8670b5073fad">COM+ Administration Collections</a>.

If you add a new object and save it with the key property of an existing object, you overwrite the existing object.




## -see-also




<a href="https://msdn.microsoft.com/fe3f7452-57b2-4f9e-9b48-5dedfe519ac1">ICatalogObject</a>
 

 

