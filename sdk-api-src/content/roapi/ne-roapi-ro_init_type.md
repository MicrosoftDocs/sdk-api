---
UID: NE:roapi.RO_INIT_TYPE
title: RO_INIT_TYPE
author: windows-driver-content
description: Determines the concurrency model used for incoming calls to the objects created by this thread.
old-location: winrt\ro_init_type.htm
old-project: WinRT
ms.assetid: 961ABFEB-E11F-4405-A021-F3756A79AF18
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: RO_INIT_MULTITHREADED, RO_INIT_TYPE, RO_INIT_TYPE enumeration [Windows Runtime], roapi/RO_INIT_MULTITHREADED, roapi/RO_INIT_TYPE, winrt.ro_init_type, winrt.winrt_init_type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: roapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RO_INIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	roapi.h
api_name:
-	RO_INIT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RO_INIT_TYPE enumeration


## -description


Determines the concurrency model used for incoming calls to the objects created by this thread.


## -enum-fields




### -field RO_INIT_SINGLETHREADED


### -field RO_INIT_MULTITHREADED

Initializes the thread for multi-threaded concurrency. The current thread is initialized in the MTA.


## -remarks



Pass the <b>RO_INIT_TYPE</b> enumeration to the <a href="https://msdn.microsoft.com/527A7FF7-749D-4178-A397-5C538F6031F8">RoInitialize</a> function to initialize a thread in the Windows Runtime.




## -see-also




<a href="https://msdn.microsoft.com/527A7FF7-749D-4178-A397-5C538F6031F8">RoInitialize</a>
 

 

