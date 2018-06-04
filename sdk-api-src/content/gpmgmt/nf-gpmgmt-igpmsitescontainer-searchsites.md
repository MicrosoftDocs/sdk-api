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

# IGPMSitesContainer::SearchSites


## -description


Retrieves a collection of scope of management (SOM) objects based on the specified search criteria. This method returns only site objects.


## -parameters




### -param pIGPMSearchCriteria [in]

Pointer to criteria to supply to the search. Valid criteria for the search include the following.



#### somLinks

Pointer to an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> or an <a href="_com_iunknown">IUnknown</a> interface to query the 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a> interface. For script programmers, this is a reference to a <b>GPMGPO</b> object.  Valid criteria includes the opContains search operator.


### -param ppIGPMSOMCollection [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/079f2fd9-7b1e-4bb1-b342-8ed8fb2c773d">IGPMSOMCollection</a> interface.


#### - objGPMSearchCriteria


<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> object to supply to the search.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMSOMCollection</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMSOMCollection</b> object.




## -see-also




<a href="https://msdn.microsoft.com/079f2fd9-7b1e-4bb1-b342-8ed8fb2c773d">IGPMSOMCollection</a>



<a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">IGPMSearchCriteria</a>



<a href="https://msdn.microsoft.com/e3fdfd44-9e90-4206-b7e9-97d4ed6eb8af">IGPMSitesContainer</a>
 

 

