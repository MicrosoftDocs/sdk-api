---
UID: NF:ddraw.IDirectDrawPalette.SetEntries
title: IDirectDrawPalette::SetEntries (ddraw.h)
description: Changes entries in a DirectDrawPalette object immediately.helpviewer_keywords: ["IDirectDrawPalette interface [DirectDraw]","SetEntries method","IDirectDrawPalette.SetEntries","IDirectDrawPalette::SetEntries","SetEntries","SetEntries method [DirectDraw]","SetEntries method [DirectDraw]","IDirectDrawPalette interface","ddraw/IDirectDrawPalette::SetEntries","directdraw.idirectdrawpalette_setentries"]
old-location: directdraw\idirectdrawpalette_setentries.htm
tech.root: directdraw
ms.assetid: c12247b9-ecb3-4fdf-b25f-373da06df791
ms.date: 12/05/2018
ms.keywords: IDirectDrawPalette interface [DirectDraw],SetEntries method, IDirectDrawPalette.SetEntries, IDirectDrawPalette::SetEntries, SetEntries, SetEntries method [DirectDraw], SetEntries method [DirectDraw],IDirectDrawPalette interface, ddraw/IDirectDrawPalette::SetEntries, directdraw.idirectdrawpalette_setentries
f1_keywords:
- ddraw/IDirectDrawPalette.SetEntries
dev_langs:
- c++
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
- IDirectDrawPalette.SetEntries
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawPalette::SetEntries


## -description


Changes entries in a DirectDrawPalette object immediately.


## -parameters




### -param arg1 [in]

Currently not used and must be set to 0.


### -param arg2 [in]

First entry to be set.


### -param arg3 [in]

Number of palette entries to be changed.


### -param arg4 [in]

An array of <a href="https://docs.microsoft.com/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structures that contains the palette entries that <b>SetEntries</b> uses to change the DirectDrawPalette object. The palette entries are 1 byte each if the DDPCAPS_8BITENTRIES flag is set, and 4 bytes otherwise. Each field is a color description.


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



You must use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access the <b>SetEntries</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nn-ddraw-idirectdrawpalette">IDirectDrawPalette</a>
 

 

