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

# ClusterNetInterfaceEnum function


## -description


Enumerates the <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interfaces</a> installed on a 
    cluster, returning one name with each call.


## -parameters




### -param hNetInterfaceEnum [in]

Handle to an existing enumeration object originally returned by the 
       <a href="https://msdn.microsoft.com/fd300162-2472-4bd2-91d6-357397c4134c">ClusterNetInterfaceOpenEnum</a> function.


### -param dwIndex [in]

Index used to identify the entry to be enumerated. This parameter should be zero for the first call and then incremented for each subsequent 
       call.


### -param lpszName [out]

Pointer to a null-terminated Unicode string containing the name of the returned object.


### -param lpcchName [in, out]

Pointer to the size, in characters, of the <i>lpszName</i> buffer. On input, 
       specify the maximum number of characters the buffer can hold, including the terminating 
       <b>NULL</b>. On output, indicates the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.


## -returns



The function returns one of the following values.



