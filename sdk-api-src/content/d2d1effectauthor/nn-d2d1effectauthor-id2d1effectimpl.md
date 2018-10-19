---
UID: NN:d2d1effectauthor.ID2D1EffectImpl
title: ID2D1EffectImpl
author: windows-sdk-content
description: Allows a custom effect's interface and behavior to be specified by the effect author.
old-location: direct2d\id2d1effectimpl.htm
tech.root: direct2d
ms.assetid: 3D87A908-FC57-4AA9-A508-C402D8413363
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ID2D1EffectImpl, ID2D1EffectImpl interface [Direct2D], ID2D1EffectImpl interface [Direct2D],described, d2d1effectauthor/ID2D1EffectImpl, direct2d.id2d1effectimpl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1EffectImpl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectImpl interface


## -description


Allows a custom effect's interface and behavior to be specified by the effect author.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1EffectImpl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID2D1EffectImpl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1EffectImpl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BC5A6B97-6BA8-4C97-9F8B-D87EBCD80A98">Initialize</a>
</td>
<td align="left" width="63%">
The effect can use this method to do one time initialization tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0EBA4FDB-A9EA-4FCF-BF40-3D73ED356CD4">PrepareForRender</a>
</td>
<td align="left" width="63%">
Prepares an effect for the rendering process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3255CD0D-5B73-4020-965E-2CBBEF5BA35B">SetGraph</a>
</td>
<td align="left" width="63%">
The renderer calls this method to provide the effect implementation with a way to specify  its transform graph and transform graph changes. 

</td>
</tr>
</table> 


## -remarks



This interface is created by the effect author from a static factory registered through 
      the <a href="https://msdn.microsoft.com/9988aad6-0487-4f48-a05c-1dfb944f6ce7">ID2D1Factory::RegisterEffect</a>  method.




## -see-also




<a href="https://msdn.microsoft.com/9988aad6-0487-4f48-a05c-1dfb944f6ce7">ID2D1Factory::RegisterEffect</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

