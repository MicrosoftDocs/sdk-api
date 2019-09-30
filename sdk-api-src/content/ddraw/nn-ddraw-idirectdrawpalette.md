---
UID: NN:ddraw.IDirectDrawPalette
title: IDirectDrawPalette (ddraw.h)
author: windows-sdk-content
description: Applications use the methods of the IDirectDrawPalette interface to create DirectDrawPalette objects and work with system-level variables. This section is a reference to the methods of this interface.
old-location: directdraw\idirectdrawpalette.htm
tech.root: directdraw
ms.assetid: 82dad1d4-2368-4cb0-a45c-0de894b016b7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectDrawPalette, IDirectDrawPalette interface [DirectDraw], IDirectDrawPalette interface [DirectDraw],described, ddraw/IDirectDrawPalette, directdraw.idirectdrawpalette
ms.topic: interface
f1_keywords: 
 - "ddraw/IDirectDrawPalette"
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
 - IDirectDrawPalette
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawPalette interface


## -description


Applications use the methods of the <b>IDirectDrawPalette</b> interface to create DirectDrawPalette objects and work with system-level variables. This section is a reference to the methods of this interface. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawPalette</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectDrawPalette</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectDrawPalette</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawpalette-getcaps">GetCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the palette object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawpalette-getentries">GetEntries</a>
</td>
<td align="left" width="63%">
Retrieves palette values from a DirectDrawPalette object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawpalette-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the DirectDrawPalette object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawpalette-setentries">SetEntries</a>
</td>
<td align="left" width="63%">
Changes entries in a DirectDrawPalette object immediately.

</td>
</tr>
</table> 


## -remarks



The methods of the <b>IDirectDrawPalette</b> interface can be organized into the following groups:<table>
<tr>
<th>Group</th>
<th>Methods</th>
</tr>
<tr>
<td>Allocating memory</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawpalette-initialize">Initialize</a>
</td>
</tr>
<tr>
<td>Palette capabilities</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawpalette-getcaps">GetCaps</a>
</td>
</tr>
<tr>
<td>Palette entries</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawpalette-getentries">GetEntries</a> and <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawpalette-setentries">SetEntries</a>
</td>
</tr>
</table>
 



You can use the LPDIRECTDRAWPALETTE data type to declare a variable that contains a pointer to an <b>IDirectDrawPalette</b> interface. The Ddraw.h header file declares the data type with the following code:




```

typedef struct IDirectDrawPalette    FAR *LPDIRECTDRAWPALETTE;

```




