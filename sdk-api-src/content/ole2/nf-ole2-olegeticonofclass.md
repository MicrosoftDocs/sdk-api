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

# OleGetIconOfClass function


## -description


Returns a handle to a metafile containing an icon and a string label for the specified CLSID.


## -parameters




### -param rclsid [in]

The CLSID for which the icon and string are to be requested.


### -param lpszLabel [in, optional]

A pointer to the label for the icon.


### -param fUseTypeAsLabel [in]

Indicates whether to use the user type string in the CLSID as the icon label.


## -returns



If the function succeeds, the return value is a handle to a metafile that contains and icon and label for the specified CLSID. Otherwise, the function returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/2fa9cd75-4dc6-45a3-aa62-e82bd28289a5">OleGetIconOfFile</a>



<a href="https://msdn.microsoft.com/627a79eb-46dd-4df7-a0d6-cab37b73387a">OleMetafilePictFromIconAndLabel</a>
 

 

