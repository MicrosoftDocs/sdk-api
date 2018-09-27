---
UID: NF:mmiscapi.sndOpenSound
title: sndOpenSound function
author: windows-sdk-content
description: Opens the specified sound event.
old-location: multimedia\sndopensound.htm
tech.root: Multimedia
ms.assetid: 59871C13-4275-4E69-AFE5-989998C9AB69
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: mmiscapi/sndOpenSound, multimedia.sndopensound, sndOpenSound, sndOpenSound function [Windows Multimedia]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mmiscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmmbse.lib
req.dll: Winmmbse.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - winmmbse.dll
 - API-MS-Win-mm-misc-l1-1-1.dll
 - winmmbase.dll
api_name:
 - sndOpenSound
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# sndOpenSound function


## -description


Opens the specified sound event.


## -parameters




### -param EventName

The name of the sound event.


### -param AppName

The application associated with the sound event.


### -param Flags

Flags for playing the sound. The following values are defined.


### -param FileHandle

Receives the handle to the sound.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



