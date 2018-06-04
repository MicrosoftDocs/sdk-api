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

# _SP_DEVINFO_DATA structure


## -description


An SP_DEVINFO_DATA structure defines a device instance that is a member of a device information set.


## -struct-fields




### -field cbSize

The size, in bytes, of the SP_DEVINFO_DATA structure. For more information, see the following Remarks section.


### -field ClassGuid

The GUID of the device's setup class.


### -field DevInst

An opaque handle to the device instance (also known as a handle to the <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">devnode</a>). 

Some functions, such as <b>SetupDi</b><i>Xxx</i> functions, take the whole SP_DEVINFO_DATA structure as input to identify a device in a device information set. Other functions, such as <b>CM</b>_<i>Xxx</i> functions like <a href="https://msdn.microsoft.com/library/windows/hardware/ff538514">CM_Get_DevNode_Status</a>, take this <b>DevInst</b> handle as input.


### -field Reserved

Reserved. For internal use only.


## -remarks



An SP_DEVINFO_DATA structure identifies a device in a device information set. For example, when Windows sends a <a href="https://msdn.microsoft.com/library/windows/hardware/ff543692">DIF_INSTALLDEVICE</a> request to a class installer and co-installers, it includes a handle to a device information set and a pointer to an SP_DEVINFO_DATA that specifies the particular device. In addition to DIF requests, this structure is also used in some <b>SetupDi</b><i>Xxx</i> functions.

<b>SetupDi</b><i>Xxx</i> functions that take an SP_DEVINFO_DATA structure as a parameter verify that the <b>cbSize</b> member of the supplied structure is equal to the size, in bytes, of the structure. If the <b>cbSize</b> member is not set correctly for an input parameter, the function will fail and set an error code of ERROR_INVALID_PARAMETER. If the <b>cbSize</b> member is not set correctly for an output parameter, the function will fail and set an error code of ERROR_INVALID_USER_BUFFER. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552345">SP_DEVINFO_LIST_DETAIL_DATA</a>
 

 

