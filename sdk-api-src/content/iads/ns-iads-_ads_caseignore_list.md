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

# _ADS_CASEIGNORE_LIST structure


## -description


The <b>ADS_CASEIGNORE_LIST</b> structure is an ADSI representation of the <b>Case Ignore List</b> attribute syntax.


## -struct-fields




### -field Next

Pointer to the next <b>ADS_CASEIGNORE_LIST</b> in the list of case-insensitive strings.


### -field String

The null-terminated Unicode string value of the current entry of the list.


## -remarks



A <b>Case Ignore List</b> attribute represents an ordered sequence of case insensitive strings.




## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>
 

 

