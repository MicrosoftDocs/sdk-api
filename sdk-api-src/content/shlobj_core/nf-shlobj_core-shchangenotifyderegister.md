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

# SHChangeNotifyDeregister function


## -description


Unregisters the client's window process from receiving <a href="https://msdn.microsoft.com/a9222ce9-0d06-4fd0-af3a-fd0e979713ce">SHChangeNotify</a> messages.


## -parameters




### -param ulID

Type: <b>ULONG</b>

A value of type <b>ULONG</b> that specifies the registration ID returned by <a href="https://msdn.microsoft.com/73143865-ca2f-4578-a7a2-2ba4833eddd8">SHChangeNotifyRegister</a>.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the specified client was found and removed; otherwise <b>FALSE</b>.




## -remarks



See the <a href="https://msdn.microsoft.com/02A7C5B4-94F2-4c35-9290-4C816E5CF63A">Change Notify Watcher Sample</a> in the Windows Software Development Kit (SDK) for a full example that demonstrates the use of this function.

The <b>NTSHChangeNotifyDeregister</b> function, which is no longer available for use as of Windows Vista, was equivalent to <b>SHChangeNotifyDeregister</b>.



