---
UID: NF:ddraw.IDirectDrawPalette.GetEntries
title: IDirectDrawPalette::GetEntries (ddraw.h)
author: windows-sdk-content
description: Retrieves palette values from a DirectDrawPalette object.
old-location: directdraw\idirectdrawpalette_getentries.htm
tech.root: directdraw
ms.assetid: ae3c639f-beb4-40b6-a237-60d6e560a1c3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetEntries, GetEntries method [DirectDraw], GetEntries method [DirectDraw],IDirectDrawPalette interface, IDirectDrawPalette interface [DirectDraw],GetEntries method, IDirectDrawPalette.GetEntries, IDirectDrawPalette::GetEntries, ddraw/IDirectDrawPalette::GetEntries, directdraw.idirectdrawpalette_getentries
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawPalette.GetEntries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawPalette::GetEntries


## -description


Retrieves palette values from a DirectDrawPalette object.



## -parameters




### -param arg1 [in]

Currently not used and must be set to 0.


### -param arg2 [in]

Start of the entries to be retrieved sequentially.


### -param arg3 [in]

Number of palette entries that can fit in the array that <i>lpEntries</i> specifies. The colors of the palette entries are returned in sequence, from the value of the <i>dwStartingEntry</i> parameter through the value of the <i>dwCount</i> parameter minus 1. (These parameters are set by <a href="https://msdn.microsoft.com/c12247b9-ecb3-4fdf-b25f-373da06df791">IDirectDrawPalette::SetEntries</a>.) 



### -param arg4 [out]

An array of <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures that receives the palette entries from the DirectDrawPalette object. The palette entries are 1 byte each if the DDPCAPS_8BITENTRIES flag is set, and 4 bytes otherwise. Each field is a color description.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOTPALETTIZED</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>GetEntries</b> method.




## -see-also




<a href="https://msdn.microsoft.com/82dad1d4-2368-4cb0-a45c-0de894b016b7">IDirectDrawPalette</a>
 

 

