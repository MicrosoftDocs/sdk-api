---
UID: NF:shdeprecated.ITravelLog.FindTravelEntry
title: ITravelLog::FindTravelEntry
author: windows-sdk-content
description: Deprecated. Determines whether a specific travel entry is present in the travel log.
old-location: shell\ITravelLog_FindTravelEntry.htm
tech.root: shell
ms.assetid: 128627f3-c010-4b8e-b067-fdc1eed346e4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: FindTravelEntry, FindTravelEntry method [Windows Shell], FindTravelEntry method [Windows Shell],ITravelLog interface, ITravelLog interface [Windows Shell],FindTravelEntry method, ITravelLog.FindTravelEntry, ITravelLog::FindTravelEntry, shdeprecated/ITravelLog::FindTravelEntry, shell.ITravelLog_FindTravelEntry, zone_ITravelLog_FindTravelEntry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - ITravelLog.FindTravelEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shdeprecated.h
: 
- ITravelLog.FindTravelEntry
: 
req.product: Internet Explorer 4.0
---

# ITravelLog::FindTravelEntry


## -description


Deprecated. Determines whether a specific travel entry is present in the travel log.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> representing the nearest browser or frame within which the travel generating the log is taking place.


### -param pidl [in]

Type: <b>LPCITEMIDLIST</b>

A PIDL of the travel entry, typically obtained through <a href="https://msdn.microsoft.com/9a3a156f-4d61-4987-b1d8-9e77564d3962">GetPidl</a>.


### -param ppte [out]

Type: <b><a href="https://msdn.microsoft.com/b8a5d532-c1fd-4302-b983-cc9a74270321">ITravelEntry</a>**</b>

The address of a pointer to the <a href="https://msdn.microsoft.com/b8a5d532-c1fd-4302-b983-cc9a74270321">ITravelEntry</a> interface representing the travel entry, if found.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



