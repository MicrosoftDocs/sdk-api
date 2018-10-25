---
UID: NE:wtsapi32._WTS_TYPE_CLASS
title: "_WTS_TYPE_CLASS"
author: windows-sdk-content
description: Specifies the type of structure that a Remote Desktop Services function has returned in a buffer.
old-location: termserv\wts_type_class.htm
tech.root: termserv
ms.assetid: 1827e862-add0-4271-b5d7-62834c396250
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: WTSTypeProcessInfoLevel0, WTSTypeProcessInfoLevel1, WTSTypeSessionInfoLevel1, WTS_TYPE_CLASS, WTS_TYPE_CLASS enumeration [Remote Desktop Services], _WTS_TYPE_CLASS, termserv.wts_type_class, wtsapi32/WTSTypeProcessInfoLevel0, wtsapi32/WTSTypeProcessInfoLevel1, wtsapi32/WTSTypeSessionInfoLevel1, wtsapi32/WTS_TYPE_CLASS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
 - Wtsapi32.h
api_name:
 - WTS_TYPE_CLASS
product: Windows
targetos: Windows
req.typenames: WTS_TYPE_CLASS
req.redist: 
---

# _WTS_TYPE_CLASS enumeration


## -description


Specifies the type of structure that a Remote Desktop Services function has returned in a buffer.


## -enum-fields




### -field WTSTypeProcessInfoLevel0

The buffer contains one or more <a href="https://msdn.microsoft.com/5df01ad8-71fd-4831-8eba-1d6cabd61348">WTS_PROCESS_INFO</a> structures.


### -field WTSTypeProcessInfoLevel1

The buffer contains one or more <a href="https://msdn.microsoft.com/a678d249-4943-4d2b-9cea-87ce20177c75">WTS_PROCESS_INFO_EX</a> structures.


### -field WTSTypeSessionInfoLevel1

The buffer contains one or more <a href="https://msdn.microsoft.com/29d76033-d61d-4bc5-b47a-f7dea9543f23">WTS_SESSION_INFO_1</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/1c325174-ec08-4bbb-8e91-1a3cc9256110">WTSFreeMemory</a>



<a href="https://msdn.microsoft.com/d84a4fe3-a829-4cf3-b217-157391d0c495">WTSFreeMemoryEx</a>
 

 

