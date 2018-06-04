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

# ADsPropCheckIfWritable function


## -description


The <b>ADsPropCheckIfWritable</b> function determines if an attribute can be written.


## -parameters




### -param pwzAttr [in]

Pointer to a NULL-terminated <b>WCHAR</b> buffer that contains the name of the attribute.


### -param pWritableAttrs [in]

Pointer to the array of <a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a> structures returned by <a href="https://msdn.microsoft.com/dcc4ea8f-6924-4e26-a675-ce326f35933c">ADsPropGetInitInfo</a>.


## -returns



Returns nonzero if the attribute is found in the writable-attribute list or zero otherwise. Also returns zero if <i>pWritableAttrs</i> is <b>NULL</b>.




## -remarks



During initialization, a property sheet extension should determine if the attributes it can change can be written by using <b>ADsPropCheckIfWritable</b>. If an attribute cannot be written, it should be displayed as read-only and the ability to change the attribute value should be removed.

It is possible for a user to be  granted write permission, but not read permission for an attribute. In this case, the attribute read operation fails and it is possible that the attribute could be overwritten. Consequently, it is not recommended to grant a user write permission, but revoke read permission on an attribute.

Do not use this function to verify the write permission for attributes in a multi-select property sheet. It is likely that each directory object will have a different set of writable attribute permissions. The property sheet extension should rely on the server returning an error when attempting to write to a specific object in a selected group to determine if write permissions for that object are denied.




## -see-also




<a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a>



<a href="https://msdn.microsoft.com/dcc4ea8f-6924-4e26-a675-ce326f35933c">ADsPropGetInitInfo</a>
 

 

