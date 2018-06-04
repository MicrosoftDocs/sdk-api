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

# lineproviderentry_tag structure


## -description


The 
<b>LINEPROVIDERENTRY</b> structure provides the information for a single service provider entry. An array of these structures is returned as part of the 
<a href="https://msdn.microsoft.com/75790ffd-bb1b-4efc-a905-5727d31f8aec">LINEPROVIDERLIST</a> structure returned by the function 
<a href="https://msdn.microsoft.com/87d43409-e8c5-401a-87a2-02568ed0af4a">lineGetProviderList</a>.


## -struct-fields




### -field dwPermanentProviderID

Permanent provider identifier of the entry.


### -field dwProviderFilenameSize

Size of the provider file name string, including the <b>null</b> terminator, in bytes.


### -field dwProviderFilenameOffset

Offset from the beginning of the 
<a href="https://msdn.microsoft.com/75790ffd-bb1b-4efc-a905-5727d31f8aec">LINEPROVIDERLIST</a> structure to a <b>null</b>-terminated string containing the file name (path) of the service provider DLL (.TSP) file. The size of the string is specified by <b>dwProviderFilenameSize</b>.


## -remarks



Not extensible.




## -see-also




<a href="https://msdn.microsoft.com/75790ffd-bb1b-4efc-a905-5727d31f8aec">LINEPROVIDERLIST</a>



<a href="https://msdn.microsoft.com/87d43409-e8c5-401a-87a2-02568ed0af4a">lineGetProviderList</a>
 

 

