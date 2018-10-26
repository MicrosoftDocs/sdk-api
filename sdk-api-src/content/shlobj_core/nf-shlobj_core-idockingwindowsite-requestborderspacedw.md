---
UID: NF:shlobj_core.IDockingWindowSite.RequestBorderSpaceDW
title: IDockingWindowSite::RequestBorderSpaceDW
author: windows-sdk-content
description: Approves, modifies, or refuses a request for an IDockingWindow object's border space. The border space is not allocated until the SetBorderSpaceDW method is called.
old-location: shell\IDockingWindowSite_RequestBorderSpaceDW.htm
tech.root: shell
ms.assetid: a104c58b-44da-47e7-b10b-f0116024bee1
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IDockingWindowSite interface [Windows Shell],RequestBorderSpaceDW method, IDockingWindowSite.RequestBorderSpaceDW, IDockingWindowSite::RequestBorderSpaceDW, RequestBorderSpaceDW, RequestBorderSpaceDW method [Windows Shell], RequestBorderSpaceDW method [Windows Shell],IDockingWindowSite interface, _win32_IDockingWindowSite_RequestBorderSpaceDW, shell.IDockingWindowSite_RequestBorderSpaceDW, shlobj_core/IDockingWindowSite::RequestBorderSpaceDW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDockingWindowSite.RequestBorderSpaceDW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDockingWindowSite::RequestBorderSpaceDW


## -description


Approves, modifies, or refuses a request for an <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> object's border space. The border space is not allocated until the <a href="https://msdn.microsoft.com/8c79c983-8a5d-4b52-848d-c85c4e4f86ec">SetBorderSpaceDW</a> method is called.


## -parameters




### -param punkObj [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> object for which the border space is being requested.


### -param pbw [in]

Type: <b>LPCBORDERWIDTHS</b>

A pointer to a <a href="https://msdn.microsoft.com/f86321d9-5706-4641-b3c9-981a8acacff6">BORDERWIDTHS</a> structure. Before calling this method, the structure must be filled with the desired border space. After the method returns successfully, the structure contains the approved border space. The <a href="https://msdn.microsoft.com/7418a6af-74ce-4435-8ed9-af106df0f95b">IDockingWindowSite</a> object may change these values. If border space is critical, it is the caller's responsibility to determine if the returned border space is sufficient.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the border space request is approved or modified, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/d0dc10db-316a-4eaa-83db-3f186ee77071">IDockingWindowFrame</a>



<a href="https://msdn.microsoft.com/7418a6af-74ce-4435-8ed9-af106df0f95b">IDockingWindowSite</a>
 

 

