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



