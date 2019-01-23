---
UID: NN:ddraw.IDirectDrawColorControl
title: IDirectDrawColorControl
author: windows-sdk-content
description: Applications use the methods of the IDirectDrawColorControl interface to get and set color controls.
old-location: directdraw\idirectdrawcolorcontrol.htm
tech.root: directdraw
ms.assetid: e9bd0dc6-2d8a-452b-894d-72a3d7a20100
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectDrawColorControl, IDirectDrawColorControl interface [DirectDraw], IDirectDrawColorControl interface [DirectDraw],described, ddraw/IDirectDrawColorControl, directdraw.idirectdrawcolorcontrol
ms.topic: interface
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
 - IDirectDrawColorControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawColorControl interface


## -description


Applications use the methods of the <b>IDirectDrawColorControl</b> interface to get and set color controls.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawColorControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectDrawColorControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectDrawColorControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16ac7bef-e88c-47da-8db9-9e6258a381a0">GetColorControls</a>
</td>
<td align="left" width="63%">
Retrieves the current color-control settings that are associated with an overlay or a primary surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de6f8266-d712-40bd-8230-cf5800cf8926">SetColorControls</a>
</td>
<td align="left" width="63%">
Sets the color-control options for an overlay or a primary surface.

</td>
</tr>
</table> 


## -remarks



You can use the LPDIRECTDRAWCOLORCONTROL data type to declare a variable that contains a pointer to an <b>IDirectDrawColorControl</b> interface. The Ddraw.h header file declares this data type with the following code:




```

typedef struct IDirectDrawColorControl    FAR *LPDIRECTDRAWCOLORCONTROL;

```




