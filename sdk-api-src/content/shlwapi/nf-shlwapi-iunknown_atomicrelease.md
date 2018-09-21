---
UID: NF:shlwapi.IUnknown_AtomicRelease
title: IUnknown_AtomicRelease function
author: windows-sdk-content
description: Releases a Component Object Model (COM) pointer and sets it to NULL.
old-location: shell\IUnknown_AtomicRelease.htm
tech.root: shell
ms.assetid: 6bb3f9cf-bf28-4f94-8557-56c1952384ec
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IUnknown_AtomicRelease, IUnknown_AtomicRelease function [Windows Shell], _win32_IUnknown_AtomicRelease, shell.IUnknown_AtomicRelease, shlwapi/IUnknown_AtomicRelease
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
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
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-comhelpers-l1-1-0.dll
api_name:
 - IUnknown_AtomicRelease
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUnknown_AtomicRelease function


## -description


Releases a Component Object Model (COM) pointer and sets it to <b>NULL</b>.


## -parameters




### -param ppunk [in, out, optional]

Type: <b>void**</b>

The address of a pointer to a COM interface.


## -returns



This function does not return a value.




## -remarks



If <i>ppunk</i> points to a <b>NULL</b> pointer, no operation is performed. Otherwise, <i>ppunk</i> is assumed to be the address of a COM interface pointer, derived from <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>. The function calls the interface's <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method then sets the interface pointer to <b>NULL</b>.


#### Examples

The following example uses <b>IUnknown_AtomicRelease</b> to release the stream, if it exists. If not, it does nothing.


```cpp
void sample()
{
    IStream *pstm = NULL;
    CreateStreamOnHGlobal(NULL, TRUE, &pstm);
    
    IUnknown_AtomicRelease((void**)&pstm);
    
    // At this point, pstm is NULL
}
```




