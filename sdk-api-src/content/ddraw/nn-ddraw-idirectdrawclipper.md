---
UID: NN:ddraw.IDirectDrawClipper
title: IDirectDrawClipper (ddraw.h)
description: Applications use the methods of the IDirectDrawClipper interface to manage clip lists. This section is a reference to the methods of this interface.
helpviewer_keywords: ["IDirectDrawClipper","IDirectDrawClipper interface [DirectDraw]","IDirectDrawClipper interface [DirectDraw]","described","ddraw/IDirectDrawClipper","directdraw.idirectdrawclipper"]
old-location: directdraw\idirectdrawclipper.htm
tech.root: directdraw
ms.assetid: 2e93583a-59a8-4a0f-9299-ed57fdcebf33
ms.date: 12/05/2018
ms.keywords: IDirectDrawClipper, IDirectDrawClipper interface [DirectDraw], IDirectDrawClipper interface [DirectDraw],described, ddraw/IDirectDrawClipper, directdraw.idirectdrawclipper
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
 - IDirectDrawClipper
 - ddraw/IDirectDrawClipper
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
 - IDirectDrawClipper
---

# IDirectDrawClipper interface


## -description

Applications use the methods of the <b>IDirectDrawClipper</b> interface to manage clip lists. This section is a reference to the methods of this interface.

## -inheritance

The <b>IDirectDrawClipper</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectDrawClipper</b> also has these types of members:

## -remarks

The methods of the <b>IDirectDrawClipper</b> interface can be organized into the following groups:<table>
<tr>
<th>Group</th>
<th>Methods</th>
</tr>
<tr>
<td>Allocating memory</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-initialize">Initialize</a>
</td>
</tr>
<tr>
<td>Clip list</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-getcliplist">GetClipList</a>, <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-iscliplistchanged">IsClipListChanged</a>, <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-setcliplist">SetClipList</a>,  and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-sethwnd">SetHWnd</a>
</td>
</tr>
<tr>
<td>Handles</td>
<td>
<a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-gethwnd">GetHWnd</a>
</td>
</tr>
</table>
 



You can use the LPDIRECTDRAWCLIPPER data type to declare a variable that contains a pointer to an <b>IDirectDrawClipper</b> interface. The Ddraw.h header file declares this data type with the following code:




```

typedef struct IDirectDrawClipper    FAR *LPDIRECTDRAWCLIPPER;

```
