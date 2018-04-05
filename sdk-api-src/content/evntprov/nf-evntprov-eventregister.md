---
UID: NF:evntprov.EventRegister
title: EventRegister function
author: windows-driver-content
description: Registers the provider.
old-location: etw\eventregister_func.htm
old-project: ETW
ms.assetid: 6025c3a6-7d88-49dc-bbc3-655c172dde3c
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: EventRegister, EventRegister function [ETW], base.eventregister_func, etw.eventregister_func, evntprov/EventRegister
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: evntprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EVENT_INFO_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
-	API-MS-Win-eventing-provider-l1-1-0.dll
-	API-MS-Win-Eventing-Provider-L1-1-1.dll
-	bcrypt.dll
api_name:
-	EventRegister
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EventRegister function


## -description


Registers the provider.


## -parameters




### -param ProviderId [in]

GUID that uniquely identifies the provider.


### -param EnableCallback [in, optional]

Callback that ETW  calls to notify you when a session enables or disables your provider. Can be 
      <b>NULL</b>.


### -param CallbackContext [in, optional]

Provider-defined context data to pass to the callback when the provider is enabled or disabled. Can be 
      <b>NULL</b>.


### -param RegHandle [out]

Registration handle. The handle is used by most provider function calls. Before your provider exits, you 
      must pass this handle to <a href="https://msdn.microsoft.com/fdcccf6f-2f31-4356-a4ee-3b6229c01b75">EventUnregister</a> to 
      free the handle.


## -returns



Returns ERROR_SUCCESS if successful.




## -remarks



Use this function to register your provider if you call 
    <a href="https://msdn.microsoft.com/93070eb7-c167-4419-abff-e861877dad07">EventWrite</a> to write your events.

A process can register up to 1,024 provider GUIDs; however, you should limit the number of providers that 
     your process registers to one or two. This limit includes those registered using this function and the 
     <a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a> function.

<b>Prior to Windows Vista:  </b>There is no limit to the number of providers that a process can register. 




## -see-also




<a href="https://msdn.microsoft.com/f339323e-9da9-495f-aac5-f44969a018eb">EnableCallback</a>



<a href="https://msdn.microsoft.com/fdcccf6f-2f31-4356-a4ee-3b6229c01b75">EventUnregister</a>
 

 

