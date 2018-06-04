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

# PifMgr_CloseProperties function


## -description


<p class="CCE_Message">[<b>PifMgr_CloseProperties</b> is available for use in the 

operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Closes application properties that were opened with <a href="https://msdn.microsoft.com/0bc11528-7278-4765-b3cb-671ba82c9155">PifMgr_OpenProperties</a>.


## -parameters




### -param hProps [in]

Type: <b>HANDLE</b>

A handle to the application's properties. This parameter should be set to the value that is returned by <a href="https://msdn.microsoft.com/0bc11528-7278-4765-b3cb-671ba82c9155">PifMgr_OpenProperties</a>.


### -param flOpt [in]

Type: <b>UINT</b>

A flag that specifies how the function operates.



#### CLOSEPROPS_DISCARD

Abandon cached data.



#### CLOSEPROPS_NONE

No options specified.


## -returns



Type: <b>int</b>

Returns <b>NULL</b> if successful. If unsuccessful, the functions returns the handle to the application properties that was passed as <i>hProps</i>.




## -see-also




<a href="https://msdn.microsoft.com/62933ddf-9b0d-427a-8b5f-a0117a3b4885">PifMgr_GetProperties</a>



<a href="https://msdn.microsoft.com/720ed580-1867-4651-aef6-24ac4397ad39">PifMgr_SetProperties</a>
 

 

