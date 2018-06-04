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

# IDiscRecorder::SetRecorderProperties


## -description


Accepts an 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> pointer for an object with all the properties that the application wishes to change. Sparse settings are supported. It is recommended, however, to query for a property set using 
<a href="https://msdn.microsoft.com/24d46cbc-56fd-4c9f-933c-0207dea5ada5">GetRecorderProperties</a>, modify only those settings of interest, and then call 
<b>SetRecorderProperties</b> to change all values simultaneously.


## -parameters




### -param pPropStg [in]

Pointer to the 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface that the disc recorder can use to retrieve new settings on various properties.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



Some properties are read-only, such as MaxWriteSpeed. Both read-only properties and unsupported properties are ignored without generating an error (see IMAPI_S_PROPERTIESIGNORED). For example, someone could submit a property set to this interface and attempt to change the MaxWriteSpeed and ClearlyNeverHeardOfBefore properties. Since MaxWriteSpeed is read-only and ClearlyNeverHeardOfBefore is an unknown value, both properties are ignored and the method succeeds.

After calling 
<b>SetRecorderProperties</b>, an application should verify property settings by calling 
<a href="https://msdn.microsoft.com/24d46cbc-56fd-4c9f-933c-0207dea5ada5">GetRecorderProperties</a>.




## -see-also




<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>
 

 

