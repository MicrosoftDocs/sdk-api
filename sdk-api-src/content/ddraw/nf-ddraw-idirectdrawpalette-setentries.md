---
UID: NF:ddraw.IDirectDrawPalette.SetEntries
title: IDirectDrawPalette::SetEntries
author: windows-sdk-content
description: Changes entries in a DirectDrawPalette object immediately.
old-location: directdraw\idirectdrawpalette_setentries.htm
old-project: directdraw
ms.assetid: c12247b9-ecb3-4fdf-b25f-373da06df791
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IDirectDrawPalette interface [DirectDraw],SetEntries method, IDirectDrawPalette.SetEntries, IDirectDrawPalette::SetEntries, SetEntries, SetEntries method [DirectDraw], SetEntries method [DirectDraw],IDirectDrawPalette interface, ddraw/IDirectDrawPalette::SetEntries, directdraw.idirectdrawpalette_setentries
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawPalette.SetEntries
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawPalette::SetEntries


## -description


Changes entries in a DirectDrawPalette object immediately.


## -parameters




### -param






#### - dwCount [in]

Number of palette entries to be changed.


#### - dwFlags [in]

Currently not used and must be set to 0.


#### - dwStartingEntry [in]

First entry to be set.


#### - lpEntries [in]

An array of <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures that contains the palette entries that <b>SetEntries</b> uses to change the DirectDrawPalette object. The palette entries are 1 byte each if the DDPCAPS_8BITENTRIES flag is set, and 4 bytes otherwise. Each field is a color description.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOPALETTEATTACHED</li>
<li>DDERR_NOTPALETTIZED</li>
<li>DDERR_UNSUPPORTED</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>SetEntries</b> method.




## -see-also




<a href="https://msdn.microsoft.com/82dad1d4-2368-4cb0-a45c-0de894b016b7">IDirectDrawPalette</a>
 

 

