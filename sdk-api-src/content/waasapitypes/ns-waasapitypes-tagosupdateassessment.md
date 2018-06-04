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

# tagOSUpdateAssessment structure


## -description


The <b>OSUpdateAssessment</b> structure defines how up-to-date the OS on a targeted device is. This structure is used primarily as a return value by <a href="https://msdn.microsoft.com/3123362E-6A1C-49BD-BE9C-0B8506EA944B">GetOSUpdateAssessment</a>, in order to retrieve an OS assessment in a single structure. 


## -struct-fields




### -field isEndOfSupport

<b>true</b> if the OS on the device is no longer supported by Microsoft and will no longer receive servicing updates; otherwise, <b>false</b>. 



### -field assessmentForCurrent

An <a href="https://msdn.microsoft.com/BD456DF6-4A29-41B4-8EB4-8F29910981E7">UpdateAssessment</a> structure containing an assessment against the latest update Microsoft has released. 


### -field assessmentForUpToDate

An <a href="https://msdn.microsoft.com/BD456DF6-4A29-41B4-8EB4-8F29910981E7">UpdateAssessment</a> structure containing an assessment against the latest applicable quality update for the device.


### -field securityStatus

An <a href="https://msdn.microsoft.com/157E241E-E8D8-41F8-9565-5C9298DCD1BE">UpdateAssessmentStatus</a> enumeration that details whether the device is on the latest applicable security update.


### -field assessmentTime

Timestamp when the assessment was done. 



### -field releaseInfoTime

Timestamp when the release information was updated. 



### -field currentOSBuild

The latest OS build that Microsoft has released. This value is used to determine whether a device is current.


### -field currentOSReleaseTime

The published timestamp of the release date for current OS build.


### -field upToDateOSBuild

The latest applicable OS build in the device's servicing train. This value is used to determine whether a device is up-to-date. 



### -field upToDateOSReleaseTime

The published timestamp of the release date for the up-to-date OS build. 


