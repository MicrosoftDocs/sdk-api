---
UID: NN:ddraw.IDirectDrawPalette
title: IDirectDrawPalette (ddraw.h)
description: Applications use the methods of the IDirectDrawPalette interface to create DirectDrawPalette objects and work with system-level variables. This section is a reference to the methods of this interface.
helpviewer_keywords: ["IDirectDrawPalette","IDirectDrawPalette interface [DirectDraw]","IDirectDrawPalette interface [DirectDraw]","described","ddraw/IDirectDrawPalette","directdraw.idirectdrawpalette"]
old-location: directdraw\idirectdrawpalette.htm
tech.root: directdraw
ms.assetid: 82dad1d4-2368-4cb0-a45c-0de894b016b7
ms.date: 12/05/2018
ms.keywords: IDirectDrawPalette, IDirectDrawPalette interface [DirectDraw], IDirectDrawPalette interface [DirectDraw],described, ddraw/IDirectDrawPalette, directdraw.idirectdrawpalette
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawPalette
 - ddraw/IDirectDrawPalette
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawPalette
---

# IDirectDrawPalette interface


## -description

Applications use the methods of the <b>IDirectDrawPalette</b> interface to create DirectDrawPalette objects and work with system-level variables. This section is a reference to the methods of this interface.

## -inheritance

The <b>IDirectDrawPalette</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectDrawPalette</b> also has these types of members:

## -remarks

The methods of the <b>IDirectDrawPalette</b> interface can be organized into the following groups:<table>
<tr>
<th>Group</th>
<th>Methods</th>
</tr>
<tr>
<td>Allocating memory</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawpalette-initialize">Initialize</a>
</td>
</tr>
<tr>
<td>Palette capabilities</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawpalette-getcaps">GetCaps</a>
</td>
</tr>
<tr>
<td>Palette entries</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawpalette-getentries">GetEntries</a> and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawpalette-setentries">SetEntries</a>
</td>
</tr>
</table>
 



You can use the LPDIRECTDRAWPALETTE data type to declare a variable that contains a pointer to an <b>IDirectDrawPalette</b> interface. The Ddraw.h header file declares the data type with the following code:




```

typedef struct IDirectDrawPalette    FAR *LPDIRECTDRAWPALETTE;

```
