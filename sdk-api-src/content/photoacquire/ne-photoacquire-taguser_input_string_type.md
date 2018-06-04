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

# tagUSER_INPUT_STRING_TYPE enumeration


## -description



The <code>USER_INPUT_STRING_TYPE</code> enumeration type indicates the type of string to obtain from the user in <a href="https://msdn.microsoft.com/db0d924b-a586-4f81-a367-e8fbdf3e9bd9">IPhotoAcquireProgressCB::GetUserInput</a>.




## -enum-fields




### -field USER_INPUT_DEFAULT

Indicates that any string is allowed.


### -field USER_INPUT_PATH_ELEMENT

Indicates that the string will not accept characters that are illegal in file or directory names (such as * or /).


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/db0d924b-a586-4f81-a367-e8fbdf3e9bd9">IPhotoAcquireProgressCB::GetUserInput</a>



<a href="https://msdn.microsoft.com/57f0c750-9c66-4c30-adc1-0cfd23d878d1">IUserInputString::GetStringType</a>
 

 

