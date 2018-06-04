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

# PENUM_PAGE_FILE_CALLBACKA callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/9289fe3c-a7d9-4acb-aeb6-a50de65db0a2">EnumPageFiles</a> function.

The <b>PENUM_PAGE_FILE_CALLBACK</b> type defines a pointer to this callback function. 
<b>EnumPageFilesProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param pContext [in]

The user-defined data passed from 
<a href="https://msdn.microsoft.com/9289fe3c-a7d9-4acb-aeb6-a50de65db0a2">EnumPageFiles</a>.


### -param pPageFileInfo [in]

A pointer to an 
<a href="https://msdn.microsoft.com/020f3be8-f624-4788-8079-0f7679c9bef0">ENUM_PAGE_FILE_INFORMATION</a> structure.


### -param lpFilename [in]

The name of the pagefile.


## -returns



To continue enumeration, the callback function must return TRUE.

To stop enumeration, the callback function must return FALSE.




## -see-also




<a href="https://msdn.microsoft.com/020f3be8-f624-4788-8079-0f7679c9bef0">ENUM_PAGE_FILE_INFORMATION</a>



<a href="https://msdn.microsoft.com/9289fe3c-a7d9-4acb-aeb6-a50de65db0a2">EnumPageFiles</a>



<a href="https://msdn.microsoft.com/e158792b-fec2-498d-aae3-d5679fa55783">PSAPI Functions</a>
 

 

