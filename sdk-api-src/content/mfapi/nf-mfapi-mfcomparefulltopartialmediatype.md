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

# MFCompareFullToPartialMediaType function


## -description



Compares a full media type to a partial media type.




## -parameters




### -param pMFTypeFull

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the full media type.


### -param pMFTypePartial

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the partial media type.


## -returns



If the full media type is compatible with the partial media type, the function returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.




## -remarks



A pipeline component can return a partial media type to describe a range of possible formats the component might accept. A partial media type has at least a major type GUID, but might be missing some of the other attributes that are needed to fully describe the type. The missing attributes represent "don't care" values for the partial type. For example, a partial video type might be missing the attributes for the width and height of the video.

This function returns <b>TRUE</b> if the following conditions are both true:

<ul>
<li>
            The partial media type contains a major type GUID.
          </li>
<li>
            All of the attributes in the partial type exist in the full type and are set to the same value.
          </li>
</ul>

        Otherwise, the function returns <b>FALSE</b>.
      




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

