---
UID: NF:shlobj_core.SHGetMalloc
title: SHGetMalloc function
author: windows-sdk-content
description: Retrieves a pointer to the Shell's IMalloc interface.
old-location: shell\SHGetMalloc.htm
tech.root: shell
ms.assetid: 720cacb9-af54-41b7-9fb6-72dfa634c4c5
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: SHGetMalloc, SHGetMalloc function [Windows Shell], _win32_SHGetMalloc, shell.SHGetMalloc, shlobj_core/SHGetMalloc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetMalloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHGetMalloc function


## -description


<p class="CCE_Message">[<b>SHGetMalloc</b> is available through Windows Vista and Windows Server 2003, but may be altered or unavailable in subsequent versions of the operating system or product. See the Remarks section for alternate recommendations.]

Retrieves a pointer to the Shell's <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> interface.
  		    
            


## -parameters




### -param ppMalloc

Type: <b>LPMALLOC*</b>

The address of a pointer that receives the Shell's <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>SHGetMalloc</b> was introduced in Windows 95 and Microsoft Windows NT 4.0, but as of Windows 2000 it is no longer necessary. In its place, programs can call the equivalent (and easier to use) <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. If you find an older reference document that suggests or even requires the use of <b>SHGetMalloc</b>, it is acceptable and encouraged to use <b>CoTaskMemAlloc</b> and <b>CoTaskMemFree</b> instead.



