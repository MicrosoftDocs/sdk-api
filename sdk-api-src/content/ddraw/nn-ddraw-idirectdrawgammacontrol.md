---
UID: NN:ddraw.IDirectDrawGammaControl
title: IDirectDrawGammaControl
author: windows-sdk-content
description: Applications use the methods of the IDirectDrawGammaControl interface to adjust the red, green, and blue gamma ramp levels of the primary surface. This section is a reference to the methods of this interface.
old-location: directdraw\idirectdrawgammacontrol.htm
old-project: directdraw
ms.assetid: a6286a2d-76d5-49ec-afd5-cbf112528db8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDirectDrawGammaControl, IDirectDrawGammaControl interface [DirectDraw], IDirectDrawGammaControl interface [DirectDraw],described, ddraw/IDirectDrawGammaControl, directdraw.idirectdrawgammacontrol
ms.prod: windows
ms.technology: windows-sdk
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
 - IDirectDrawGammaControl
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawGammaControl interface


## -description


Applications use the methods of the <b>IDirectDrawGammaControl</b> interface to adjust the red, green, and blue gamma ramp levels of the primary surface. This section is a reference to the methods of this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawGammaControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectDrawGammaControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectDrawGammaControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba83605c-c388-42c0-9297-1666c80a278e">GetGammaRamp</a>
</td>
<td align="left" width="63%">
Retrieves the red, green, and blue gamma ramps for the primary surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bde7ba7-8498-42e5-bd5a-625e162fc1db">SetGammaRamp</a>
</td>
<td align="left" width="63%">
Sets the red, green, and blue gamma ramps for the primary surface.


</td>
</tr>
</table> 


## -remarks



The <b>IDirectDrawGammaControl</b> interface is supported by DirectDrawSurface objects. That is, you can retrieve a pointer to the <b>IDirectDrawGammaControl</b> interface by calling the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method of a DirectDrawSurface object and by specifying the IID_IDirectDrawGammaControl reference identifier in the <i>riid</i> parameter.



You can use the LPDIRECTDRAWGAMMACONTROL data type to declare a variable that contains a pointer to an <b>IDirectDrawGammaControl</b> interface. The Ddraw.h header file declares the data type with the following code:



<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef struct IDirectDrawGammaControl    FAR *LPDIRECTDRAWGAMMACONTROL;
</pre>
</td>
</tr>
</table></span></div>


