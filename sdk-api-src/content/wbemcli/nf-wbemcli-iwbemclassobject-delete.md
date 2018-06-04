---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# IWbemClassObject::Delete


## -description


The 
<b>IWbemClassObject::Delete</b> method deletes the specified property from a CIM class definition and all of its qualifiers. Because instances cannot have contents that are different from the owning class, delete operations for properties are only possible on class definitions. If you invoke 
<b>Delete</b> on a property in an instance, the operation succeeds; however, rather than removing the value, it is simply reset to the default value for the class.

It is not possible to delete a property inherited from a parent class. However, if an override default value for a property inherited from a parent class was specified, it is possible to revert to the parent's default value by invoking this method. In this case, <b>WBEM_S_RESET_TO_DEFAULT</b> is returned.


<a href="https://msdn.microsoft.com/e812c0cb-3e08-4cac-8d05-2cd7abc922d1">System properties</a> cannot be deleted.


## -parameters




### -param wszName [in]

Property name to delete. This must point to a valid <b>LPCWSTR</b>. It is treated as read-only.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/e812c0cb-3e08-4cac-8d05-2cd7abc922d1">WMI System Properties</a>
 

 

