---
UID: NE:roapi.RO_INIT_TYPE
title: RO_INIT_TYPE (roapi.h)
author: windows-sdk-content
description: Determines the concurrency model used for incoming calls to the objects created by this thread.
old-location: winrt\ro_init_type.htm
tech.root: WinRT
ms.assetid: 961ABFEB-E11F-4405-A021-F3756A79AF18
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RO_INIT_MULTITHREADED, RO_INIT_TYPE, RO_INIT_TYPE enumeration [Windows Runtime], roapi/RO_INIT_MULTITHREADED, roapi/RO_INIT_TYPE, winrt.ro_init_type, winrt.winrt_init_type
ms.topic: enum
f1_keywords: 
 - "roapi/RO_INIT_TYPE"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - roapi.h
api_name:
 - RO_INIT_TYPE
targetos: Windows
req.typenames: RO_INIT_TYPE
req.redist: 
ms.custom: 19H1
---

# RO_INIT_TYPE enumeration


## -description


Determines the concurrency model used for incoming calls to the objects created by this thread.


## -enum-fields




### -field RO_INIT_SINGLETHREADED


### -field RO_INIT_MULTITHREADED

Initializes the thread for multi-threaded concurrency. The current thread is initialized in the MTA.


## -remarks



Pass the <b>RO_INIT_TYPE</b> enumeration to the <a href="https://docs.microsoft.com/windows/desktop/api/roapi/nf-roapi-roinitialize">RoInitialize</a> function to initialize a thread in the Windows Runtime.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/roapi/nf-roapi-roinitialize">RoInitialize</a>
 

 

