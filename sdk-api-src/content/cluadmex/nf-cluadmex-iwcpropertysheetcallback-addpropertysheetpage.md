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

# IWCPropertySheetCallback::AddPropertySheetPage


## -description


Adds a property page to a 
    <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> property sheet.


## -parameters




### -param hpage [in]

Handle to the property page to be added.


## -returns



If 
       <b>AddPropertySheetPage</b> 
       was not successful, it can return other <b>HRESULT</b> values.




## -remarks



Call the 
     <b>AddPropertySheetPage</b> 
     method from your 
     <a href="https://msdn.microsoft.com/00eca370-a2c6-4f5c-94a9-7d7e4334ccd5">IWEExtendPropertySheet::CreatePropertySheetPages</a> 
     implementation. However, before you call 
     <b>AddPropertySheetPage</b>, 
     call the function <a href="_win32_createpropertysheetpage_cpp">CreatePropertySheetPage</a> 
     to retrieve a handle to pass in the <i>hpage</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/f90f9eb3-5568-4db1-8ff8-fda2d3bea952">IWCPropertySheetCallback</a>



<a href="https://msdn.microsoft.com/00eca370-a2c6-4f5c-94a9-7d7e4334ccd5">IWEExtendPropertySheet::CreatePropertySheetPages</a>
 

 

