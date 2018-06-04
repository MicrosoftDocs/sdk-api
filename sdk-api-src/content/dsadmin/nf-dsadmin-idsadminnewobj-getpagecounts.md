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

# IDsAdminNewObj::GetPageCounts


## -description


The <b>IDsAdminNewObj::GetPageCounts</b> method obtains the total number of pages in the wizard as well as the index of the first page of the  extension.


## -parameters




### -param pnTotal [out]

Pointer to a <b>LONG</b> value that receives the total number of pages contained in the wizard.


### -param pnStartIndex [out]

Pointer to a <b>LONG</b> value that receives the zero-based index of the first page of the extension.


## -returns



This method can return one of these values.


Returns one of the following values.






## -remarks



This function will provide results based on the count of pages added using 
<a href="https://msdn.microsoft.com/4e16385f-b38a-4961-95ec-c81fd538ae2b">IDsAdminNewObjExt::AddPages</a>. If there are changes to the number of pages because of page manipulations by Win32 APIs, the supplied values may not be accurate. If this method is called in response to the <a href="https://msdn.microsoft.com/e6dbb0ed-e20e-49c7-8247-d5688be93d8e">IDsAdminNewObjExt::SetObject</a> method, the supplied page counts are most likely to be accurate.




## -see-also




<a href="https://msdn.microsoft.com/b38016a2-bbb7-4715-81cc-bd9911fb5a3b">IDsAdminNewObj</a>



<a href="https://msdn.microsoft.com/4e16385f-b38a-4961-95ec-c81fd538ae2b">IDsAdminNewObjExt::AddPages</a>



<a href="https://msdn.microsoft.com/e6dbb0ed-e20e-49c7-8247-d5688be93d8e">IDsAdminNewObjExt::SetObject</a>
 

 

