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

# lineproviderlist_tag structure


## -description


The 
<b>LINEPROVIDERLIST</b> structure describes a list of service providers. A structure of this type is returned by the 
<a href="https://msdn.microsoft.com/87d43409-e8c5-401a-87a2-02568ed0af4a">lineGetProviderList</a> function. The 
<b>LINEPROVIDERLIST</b> structure can contain an array of 
<a href="https://msdn.microsoft.com/e54a8244-e773-441f-a387-b3b22c4a0a54">LINEPROVIDERENTRY</a> structures.


## -struct-fields




### -field dwTotalSize

Total size allocated to this data structure, in bytes.


### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwNumProviders

Number of 
<a href="https://msdn.microsoft.com/e54a8244-e773-441f-a387-b3b22c4a0a54">LINEPROVIDERENTRY</a> structures present in the array denominated by <b>dwProviderListSize</b> and <b>dwProviderListOffset</b>.


### -field dwProviderListSize

Size of the provider list array, in bytes.


### -field dwProviderListOffset

Offset from the beginning of this structure to an array of 
<a href="https://msdn.microsoft.com/e54a8244-e773-441f-a387-b3b22c4a0a54">LINEPROVIDERENTRY</a> elements, which provide the information on each service provider. The size of the array is specified by <b>dwProviderListSize</b>.


## -remarks



This structure may not be extended.




## -see-also




<a href="https://msdn.microsoft.com/e54a8244-e773-441f-a387-b3b22c4a0a54">LINEPROVIDERENTRY</a>



<a href="https://msdn.microsoft.com/87d43409-e8c5-401a-87a2-02568ed0af4a">lineGetProviderList</a>
 

 

