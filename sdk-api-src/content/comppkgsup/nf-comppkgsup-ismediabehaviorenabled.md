---
UID: NF:comppkgsup.IsMediaBehaviorEnabled
title: IsMediaBehaviorEnabled function
author: windows-sdk-content
description: Gets a value indicating whether the media behavior associated with the specified GUID is enabled.
old-location: winprog\ismediabehaviorenabled.htm
tech.root: devnotes
ms.assetid: 6D1F52E3-3AC0-4270-8931-53D8687A10C7
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IsMediaBehaviorEnabled, IsMediaBehaviorEnabled function [Windows API], comppkgsup/IsMediaBehaviorEnabled, winprog.ismediabehaviorenabled
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: comppkgsup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comppkgsup.lib
req.dll: CompPkgSup.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CompPkgSup.dll
api_name:
 - IsMediaBehaviorEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- IsMediaBehaviorEnabled
: 
---

# IsMediaBehaviorEnabled function


## -description


Gets a value indicating whether the media behavior associated with the specified GUID is enabled.


## -parameters




### -param mediaBehavior

A GUID that specifies the media behavior for which the enabled state is queried.


## -returns



True if the specified media behavior is enabled; otherwise, false.




## -remarks



Currently, the only value supported for this function is  <b>MEDIA_BEHAVIOR_MEDIAPLAYBACKLIST_AUTOPLAYBACKITEMRESET</b> which causes media items in a <a href="https://docs.microsoft.com/en-us/uwp/api/Windows.Media.Playback.MediaPlaybackList">MediaPlaybackList</a> to be automatically reset after being played.



