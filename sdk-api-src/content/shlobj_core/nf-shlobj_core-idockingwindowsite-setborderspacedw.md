---
UID: NF:shlobj_core.IDockingWindowSite.SetBorderSpaceDW
title: IDockingWindowSite::SetBorderSpaceDW
author: windows-sdk-content
description: Allocates and reserves border space for an IDockingWindow object.
old-location: shell\IDockingWindowSite_SetBorderSpaceDW.htm
tech.root: shell
ms.assetid: 8c79c983-8a5d-4b52-848d-c85c4e4f86ec
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IDockingWindowSite interface [Windows Shell],SetBorderSpaceDW method, IDockingWindowSite.SetBorderSpaceDW, IDockingWindowSite::SetBorderSpaceDW, SetBorderSpaceDW, SetBorderSpaceDW method [Windows Shell], SetBorderSpaceDW method [Windows Shell],IDockingWindowSite interface, _win32_IDockingWindowSite_SetBorderSpaceDW, shell.IDockingWindowSite_SetBorderSpaceDW, shlobj_core/IDockingWindowSite::SetBorderSpaceDW
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
 - IDockingWindowSite.SetBorderSpaceDW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDockingWindowSite::SetBorderSpaceDW


## -description


Allocates and reserves border space for an <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> object.


## -parameters




### -param punkObj [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> object for which the border space is being set.


### -param pbw [in]

Type: <b>LPCBORDERWIDTHS</b>

A pointer to a <a href="https://msdn.microsoft.com/f86321d9-5706-4641-b3c9-981a8acacff6">BORDERWIDTHS</a> structure that contains the coordinates of the <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> object's border space. The border space should be approved through a successful call to the <a href="https://msdn.microsoft.com/a104c58b-44da-47e7-b10b-f0116024bee1">IDockingWindowSite::RequestBorderSpaceDW</a> method before <b>SetBorderSpaceDW</b> is called with these coordinates.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d0dc10db-316a-4eaa-83db-3f186ee77071">IDockingWindowFrame</a>



<a href="https://msdn.microsoft.com/7418a6af-74ce-4435-8ed9-af106df0f95b">IDockingWindowSite</a>
 

 

