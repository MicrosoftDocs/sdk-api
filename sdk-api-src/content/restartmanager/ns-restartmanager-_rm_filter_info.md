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

# _RM_FILTER_INFO structure


## -description


Contains information about modifications to restart or shutdown actions. Add, remove, and list modifications to specified applications and services that have been registered with the Restart Manager session by using the <a href="https://msdn.microsoft.com/63d1d1d2-d7b7-4d6c-99f9-b849229e171f">RmAddFilter</a>, <a href="https://msdn.microsoft.com/fb1baa7b-0dfb-4bd1-8a3f-cfaf9bf4079f">RmRemoveFilter</a>, and the <a href="https://msdn.microsoft.com/61427838-8b23-4105-93fd-55f457fd43a7">RmGetFilterList</a> functions.


## -struct-fields




### -field FilterAction

This member contains a <a href="https://msdn.microsoft.com/68f77dbc-14cb-4b87-9589-328b1cef38d9">RM_FILTER_ACTION</a> enumeration value. Use the value  <b>RmNoRestart</b> 
to prevent the restart of the application or service. Use the value  <b>RmNoShutdown</b> to prevent the shutdown and restart of the application or service.


### -field FilterTrigger

This member contains a <a href="https://msdn.microsoft.com/1198c52b-f5f5-46e9-878e-39143687d645">RM_FILTER_TRIGGER</a> enumeration value. Use the value  <b>RmFilterTriggerFile</b> to modify the restart or shutdown actions  of an application referenced by the executable's full path filename. Use  the value <b>RmFilterTriggerProcess</b> to modify the restart or shutdown actions   of an application referenced by a <a href="https://msdn.microsoft.com/5e3698c7-1ea8-4f9d-8fae-e69055a000fc">RM_UNIQUE_PROCESS</a> structure. Use  the value <b>RmFilterTriggerService</b> 
to modify the restart or shutdown actions of a service referenced by the short service name.


### -field cbNextOffset

The offset in bytes to the next structure.


### -field strFilename

If the value of <b>FilterTrigger</b> is <b>RmFilterTriggerFile</b>, this member contains a pointer to a string value that contains the application filename.


### -field Process

If the value of <b>FilterTrigger</b> is  <b>RmFilterTriggerProcess</b>,  this member is a  <a href="https://msdn.microsoft.com/27e593f9-8ff0-4de4-87ca-7fa5f324468a">RM_PROCESS_INFO</a> structure for the application.


### -field strServiceShortName

If the value of <b>FilterTrigger</b> is <b>RmFilterTriggerService</b> this member is a pointer to a string value that contains the short service name.


## -see-also




<a href="https://msdn.microsoft.com/1198c52b-f5f5-46e9-878e-39143687d645">RM_FILTER_TRIGGER</a>



<a href="https://msdn.microsoft.com/61427838-8b23-4105-93fd-55f457fd43a7">RmGetFilterList</a>
 

 

