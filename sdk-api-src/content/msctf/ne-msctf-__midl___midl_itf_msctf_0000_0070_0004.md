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

# __MIDL___MIDL_itf_msctf_0000_0070_0004 enumeration


## -description


Elements of the <b>TF_DA_ATTR_INFO</b> enumeration are used to specify text conversion data in the <a href="https://msdn.microsoft.com/29faaa22-ea03-4a2e-a035-7979e2a89fc9">TF_DISPLAYATTRIBUTE</a> structure.


## -enum-fields




### -field TF_ATTR_INPUT

The text is entered by the user and has not been converted yet.


### -field TF_ATTR_TARGET_CONVERTED

The user has made a character selection and the text has been converted yet.


### -field TF_ATTR_CONVERTED

The text is converted.


### -field TF_ATTR_TARGET_NOTCONVERTED

The user made a character selection, but the text is not converted yet.


### -field TF_ATTR_INPUT_ERROR

The text is an error character and cannot be converted. For example, some consonants cannot be put together.


### -field TF_ATTR_FIXEDCONVERTED

The text is not converted. Theses characters will no longer be converted.


### -field TF_ATTR_OTHER

Reserved for the system.


## -see-also




<a href="https://msdn.microsoft.com/29faaa22-ea03-4a2e-a035-7979e2a89fc9">TF_DISPLAYATTRIBUTE
      </a>
 

 

