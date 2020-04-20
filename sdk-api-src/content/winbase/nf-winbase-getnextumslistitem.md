---
UID: NF:winbase.GetNextUmsListItem
title: GetNextUmsListItem function (winbase.h)
description: Returns the next user-mode scheduling (UMS) thread context in a list of thread contexts.helpviewer_keywords: ["GetNextUmsListItem","GetNextUmsListItem function","base.getnextumslistitem","winbase/GetNextUmsListItem"]
old-location: base\getnextumslistitem.htm
tech.root: ProcThread
ms.assetid: fb2c8420-12f4-4bd7-ac00-b53bab760db0
ms.date: 12/05/2018
ms.keywords: GetNextUmsListItem, GetNextUmsListItem function, base.getnextumslistitem, winbase/GetNextUmsListItem
f1_keywords:
- winbase/GetNextUmsListItem
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetNextUmsListItem function


## -description


Returns the next user-mode scheduling (UMS) thread context in a list of thread contexts.


## -parameters




### -param UmsContext [in, out]

A pointer to a UMS context in a list of thread contexts. This list is retrieved by the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-dequeueumscompletionlistitems">DequeueUmsCompletionListItems</a> function. 


## -returns



If the function succeeds, it returns a pointer to the next thread context in the list.

If there is no thread context after the context specified by the <i>UmsContext</i> parameter,  the function returns NULL. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-dequeueumscompletionlistitems">DequeueUmsCompletionListItems</a>
 

 

