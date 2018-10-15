---
UID: NF:winbase.GetNextUmsListItem
title: GetNextUmsListItem function
author: windows-sdk-content
description: Returns the next user-mode scheduling (UMS) thread context in a list of thread contexts.
old-location: base\getnextumslistitem.htm
tech.root: ProcThread
ms.assetid: fb2c8420-12f4-4bd7-ac00-b53bab760db0
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetNextUmsListItem, GetNextUmsListItem function, base.getnextumslistitem, winbase/GetNextUmsListItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 (64-bit only) [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-ums-l1-1-0.dll
api_name:
 - GetNextUmsListItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNextUmsListItem function


## -description


Returns the next user-mode scheduling (UMS) thread context in a list of thread contexts.


## -parameters




### -param UmsContext [in, out]

A pointer to a UMS context in a list of thread contexts. This list is retrieved by the <a href="https://msdn.microsoft.com/91499eb9-9fc5-4135-95f6-1bced78f1e07">DequeueUmsCompletionListItems</a> function. 


## -returns



If the function succeeds, it returns a pointer to the next thread context in the list.

If there is no thread context after the context specified by the <i>UmsContext</i> parameter,  the function returns NULL. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/91499eb9-9fc5-4135-95f6-1bced78f1e07">DequeueUmsCompletionListItems</a>
 

 

