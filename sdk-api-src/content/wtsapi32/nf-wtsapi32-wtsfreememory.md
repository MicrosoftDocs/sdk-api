---
UID: NF:wtsapi32.WTSFreeMemory
title: WTSFreeMemory function
author: windows-sdk-content
description: Frees memory allocated by a Remote Desktop Services function.
old-location: termserv\wtsfreememory.htm
old-project: TermServ
ms.assetid: 1c325174-ec08-4bbb-8e91-1a3cc9256110
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: WTSFreeMemory, WTSFreeMemory function [Remote Desktop Services], _win32_wtsfreememory, termserv.wtsfreememory, wtsapi32/WTSFreeMemory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_VIRTUAL_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSFreeMemory
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSFreeMemory function


## -description


Frees memory allocated by a Remote Desktop Services function.


## -parameters




### -param pMemory [in]

Pointer to the memory to free.


## -returns



This function does not return a value.




## -remarks



Several Remote Desktop Services functions allocate buffers to return information. Use the 
<b>WTSFreeMemory</b> function to free these buffers.




## -see-also




<a href="https://msdn.microsoft.com/ddfae294-2e7c-416e-b328-76d011b4af39">WTSEnumerateProcesses</a>



<a href="https://msdn.microsoft.com/6f9dd7d4-48dc-411c-85f1-cd1239d1e106">WTSEnumerateSessions</a>



<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a>



<a href="https://msdn.microsoft.com/aabbcc03-3241-49ab-ab11-ccd3e6893e78">WTSQueryUserConfig</a>
 

 

