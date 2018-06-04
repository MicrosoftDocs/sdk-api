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

# DsGetFriendlyClassName function


## -description


The <b>DsGetFriendlyClassName</b> function retrieves the localized name for an object class. This function is obsolete. New applications should use the <a href="https://msdn.microsoft.com/192e2a57-6bde-4357-893e-37f466588b55">IDsDisplaySpecifier::GetFriendlyClassName</a> method to perform this function.


## -parameters




### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the object class to obtain the name of. Examples of the object class name are "user" and "container".


### -param pszBuffer [in]

Pointer to a wide character buffer that receives the name string. This buffer must be at least <i>cchBuffer</i> wide characters in length.


### -param cchBuffer [in]

Contains the size of the <i>pszBuffer</i> buffer, in wide characters, including the terminating <b>NULL</b> character. If the name exceeds this number of characters, the name is truncated.


## -returns



Returns a standard  <b>HRESULT</b> value, including the following.




## -remarks



If no friendly name is set in the display specifiers for the object class, this function returns the name passed in <i>pszObjectClass</i>.




## -see-also




<a href="https://msdn.microsoft.com/192e2a57-6bde-4357-893e-37f466588b55">IDsDisplaySpecifier::GetFriendlyClassName</a>
 

 

