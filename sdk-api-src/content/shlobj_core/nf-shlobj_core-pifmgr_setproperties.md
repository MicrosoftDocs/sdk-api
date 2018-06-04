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

# PifMgr_SetProperties function


## -description


<p class="CCE_Message">[<b>PifMgr_SetProperties</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Assigns values to a block of data from a .pif file.


## -parameters




### -param hProps [in, optional]

Type: <b>HANDLE</b>

A handle to the application's properties. This parameter should be set to the value that is returned by <a href="https://msdn.microsoft.com/0bc11528-7278-4765-b3cb-671ba82c9155">PifMgr_OpenProperties</a>.


### -param pszGroup [in, optional]

Type: <b>PCSTR</b>

A null-terminated ANSI string containing the property group name. It can be one of the following, or any other name that corresponds to a valid .pif extension.



#### 

"WINDOWS 286 3.0"

"WINDOWS 386 3.0"

"WINDOWS VMM 4.0"

"WINDOWS NT  3.1"

"WINDOWS NT  4.0"


### -param lpProps [in]

Type: <b>const void*</b>

A property group record buffer that holds the data.


### -param cbProps

Type: <b>int</b>

The size of the buffer, in bytes, pointed to by <i>lpProps</i>.


### -param flOpt

Type: <b>UINT</b>

Always SETPROPS_NONE.


## -returns



Type: <b>int</b>

Returns the amount of information transferred, in bytes. Returns zero if the group cannot be found or an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/62933ddf-9b0d-427a-8b5f-a0117a3b4885">PifMgr_GetProperties</a>
 

 

