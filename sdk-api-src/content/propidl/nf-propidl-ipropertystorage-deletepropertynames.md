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

# IPropertyStorage::DeletePropertyNames


## -description



			The <b>DeletePropertyNames</b> method deletes specified string names from the current property set.


## -parameters




### -param cpropid [in]

The size on input of the array <i>rgpropid</i>. If 0, no property names are deleted.


### -param rgpropid [in]

Property identifiers for which string names are to be deleted.


## -returns




						This method supports the standard return value E_UNEXPECTED, in addition to the following:




## -remarks



For each property identifier in <i>rgpropid</i>, <b>IPropertyStorage::DeletePropertyNames</b> removes any corresponding name-to-property ID mapping. An attempt is silently ignored to delete the name of a property that either does not exist or does not currently have a string name associated with it. This method has no effect on the properties themselves.

<div class="alert"><b>Note</b>  All the stored string property names can be deleted by deleting property identifier zero, but <i>cpropid</i> must be equal to 1 for this to be a valid parameter error.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/42b0bf7e-0402-425c-8a5f-09eaa16d93fe">IPropertyStorage::ReadPropertyNames</a>
 

 

