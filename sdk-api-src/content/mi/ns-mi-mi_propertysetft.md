---
UID: NS:mi._MI_PropertySetFT
title: MI_PropertySetFT
author: windows-sdk-content
description: A support structure used in the MI_PropertySet structure. Use the functions with the name prefix &#0034;MI_PropertySet_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_propertysetft.htm
tech.root: wmi_v2
ms.assetid: d71c0378-0b97-44ea-9f42-e533b93f195e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_PropertySetFT, MI_PropertySetFT structure [Windows Management Infrastructure (MI)], mi/MI_PropertySetFT, wmi_v2.mi_propertysetft
ms.topic: struct
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_PropertySetFT
product: Windows
targetos: Windows
req.typenames: MI_PropertySetFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_PropertySetFT structure


## -description


A support structure used in the 
     <a href="https://msdn.microsoft.com/7c9e41b0-818e-46aa-8900-5006904f78d5">MI_PropertySet</a> structure. Use the functions with the 
     name prefix "MI_PropertySet_" to manipulate these structures.


## -struct-fields




### -field MI_Result

TBD 




#### - AddElement

Adds a name to the property list. See 
       <a href="https://msdn.microsoft.com/b7676ebd-bc65-4aad-b3c7-263ceb976b20">MI_PropertySet_AddElement</a>.


#### - Clear

Removes all names from the property list. See 
       <a href="https://msdn.microsoft.com/c5cd80b7-51bc-48dd-a49d-c3ce6d92fd55">MI_PropertySet_Clear</a>.


#### - Clone

Creates a copy of the specified property set on the heap. See 
       <a href="https://msdn.microsoft.com/77e7fc5c-3fb9-4037-94b9-c93155c06416">MI_PropertySet_Clone</a>.


#### - ContainsElement

Determines whether the property list contains the specified property. See 
       <a href="https://msdn.microsoft.com/71cf9c53-4e97-432c-9dfe-bef8ba119f71">MI_PropertySet_ContainsElement</a>.


#### - Delete

Deletes the specified property list that was constructed on the heap. See 
       <a href="https://msdn.microsoft.com/8ab75a67-0b0e-443b-87b1-ca33f44dde9b">MI_PropertySet_Delete</a>.


#### - Destruct

Deletes the specified property list that was constructed on the stack. See 
       <a href="https://msdn.microsoft.com/b00eba60-5fff-4e31-acee-c9b148e9ab7c">MI_PropertySet_Destruct</a>.


#### - GetElementAt

Gets the element of a property set at the specified index. See 
       <a href="https://msdn.microsoft.com/234fe69f-cba6-4ad0-b970-f90346488417">MI_PropertySet_GetElementAt</a>.


#### - GetElementCount

Gets the number of elements in the specified property set. See 
       <a href="https://msdn.microsoft.com/450f778c-6b59-4c01-9c21-7f96f28ebe26">MI_PropertySet_GetElementCount</a>.

