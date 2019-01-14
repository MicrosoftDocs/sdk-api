---
UID: NN:d2d1effectauthor.ID2D1EffectContext
title: ID2D1EffectContext
author: windows-sdk-content
description: Provides factory methods and other state management for effect and transform authors.
old-location: direct2d\id2d1contextinternal.htm
tech.root: Direct2D
ms.assetid: 6BE6DF90-C5B7-4377-9DBF-804AB1C91FEE
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1EffectContext, ID2D1EffectContext interface [Direct2D], ID2D1EffectContext interface [Direct2D],described, d2d1effectauthor/ID2D1EffectContext, direct2d.id2d1contextinternal
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
req.lib: D2D1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.lib
 - D2D1.dll
api_name:
 - ID2D1EffectContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectContext interface


## -description


Provides factory methods and other state management for effect and transform authors.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1EffectContext</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID2D1EffectContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1EffectContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1A97B928-7715-4D4E-AD38-7D01EE243494">CheckFeatureSupport</a>
</td>
<td align="left" width="63%">
This indicates whether an optional capability is supported by the D3D device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23B8D1A5-05F4-4056-BFA8-8D9C89FE0492">CreateBlendTransform</a>
</td>
<td align="left" width="63%">
This creates a blend transform that can be inserted into a transform graph. 



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E1FC2BF9-7287-4F9B-BDCF-3CD6EC8B849D">CreateBorderTransform</a>
</td>
<td align="left" width="63%">
Creates a transform that extends its input infinitely in every direction based on the passed in extend mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6B6820E5-792F-447C-81C9-493FA572F61A">CreateBoundsAdjustmentTransform</a>
</td>
<td align="left" width="63%">
Creates and returns a bounds adjustment  transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FB06917B-091A-4429-83BA-DAEF26F654BE">CreateColorContext</a>
</td>
<td align="left" width="63%">
Creates a color context from a color space.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84B12901-48B1-4FA9-8C81-1CEA70CF2824">CreateColorContextFromFilename</a>
</td>
<td align="left" width="63%">
Creates a color context by loading it from the specified filename.  The profile bytes are the contents of the file specified by <i>filename</i>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4A269666-28A1-4A03-823B-60C6A1A9D73E">CreateColorContextFromWicColorContext</a>
</td>
<td align="left" width="63%">
Creates a color context from an <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>.  The <a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">D2D1ColorContext</a> space of the resulting context varies, see Remarks for more info.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BF903D96-F643-4C87-9191-A46B7CE3B12C">CreateEffect</a>
</td>
<td align="left" width="63%">
Creates a Direct2D effect for the specified  class ID.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A0A479F7-CB2C-4A9A-B482-2383A3A1A841">CreateOffsetTransform</a>
</td>
<td align="left" width="63%">
Creates and returns an offset transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/265888DA-03C2-42F0-92D8-FEB542F9BAA4">CreateResourceTexture</a>
</td>
<td align="left" width="63%">
Creates or finds the given resource texture, depending on whether a resource id is specified. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75F1366A-4E82-4CAD-A843-6E53035CB520">CreateTransformNodeFromEffect</a>
</td>
<td align="left" width="63%">
Wraps an effect graph into a single transform node and then inserted into a transform graph. This allows an effect to aggregate other effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8E59527F-B6CE-4E25-B7F7-2D03BC1ACAFD">CreateVertexBuffer</a>
</td>
<td align="left" width="63%">
Creates a vertex buffer or finds a standard vertex buffer and optionally initializes it with vertices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7E205798-A9E1-4213-925B-7A5DF918F60E">FindResourceTexture</a>
</td>
<td align="left" width="63%">
Finds the given resource texture if it has already been created with <a href="https://msdn.microsoft.com/265888DA-03C2-42F0-92D8-FEB542F9BAA4">ID2D1EffectContext::CreateResourceTexture</a> with the same GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8CAC0872-2368-4926-8FF9-87D73136986F">FindVertexBuffer</a>
</td>
<td align="left" width="63%">
This finds the given vertex buffer if it has already been created with <a href="https://msdn.microsoft.com/8E59527F-B6CE-4E25-B7F7-2D03BC1ACAFD">ID2D1EffectContext::CreateVertexBuffer</a> with the same GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/465D75BF-67A0-410C-950E-DB42995379B0">GetDpi</a>
</td>
<td align="left" width="63%">
Gets the unit mapping that an effect will use for properties that could be in either dots per inch (dpi) or pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BDB553F8-C19D-46FC-A3CF-7E525DA81CE2">GetMaximumSupportedFeatureLevel</a>
</td>
<td align="left" width="63%">
This indicates the maximum feature level from the provided list which is supported by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/731A7CF3-03E7-4D38-A8DD-8D207AE90B16">IsBufferPrecisionSupported</a>
</td>
<td align="left" width="63%">
 Indicates whether the buffer precision is supported by the underlying Direct2D <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">device.</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9B923E7A-FF71-4575-880F-FA6AB6C9F366">IsShaderLoaded</a>
</td>
<td align="left" width="63%">
This tests to see if the given shader is loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64CA9647-8E9E-417D-A8D4-71AAF58F1C32">LoadComputeShader</a>
</td>
<td align="left" width="63%">
Loads the given shader by its unique ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7A5F58DD-8A43-406D-AC3B-2FB99BE7FBF6">LoadPixelShader</a>
</td>
<td align="left" width="63%">
Loads the given shader by its unique ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60D3DB1B-D347-44FC-98F9-545D4213F1F0">LoadVertexShader</a>
</td>
<td align="left" width="63%">
Loads the given shader by its unique ID.

</td>
</tr>
</table> 


## -remarks



This interface  is passed to an effect implementation through the <a href="https://msdn.microsoft.com/BC5A6B97-6BA8-4C97-9F8B-D87EBCD80A98">ID2D1EffectImpl::Initialize</a> method. In order to prevent applications casually gaining access to this interface, and to separate reference counts between the public and private interfaces, it is not possible to call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> between the <a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a> and the <b>ID2D1EffectContext</b>.

Each call to <a href="https://msdn.microsoft.com/BC5A6B97-6BA8-4C97-9F8B-D87EBCD80A98">ID2D1Effect::Initialize</a> will be provided a different <b>ID2D1EffectContext</b> interface. This interface tracks resource allocations for the effect. When the effect is released, the corresponding allocations will also be released.




## -see-also




<a href="https://msdn.microsoft.com/3D87A908-FC57-4AA9-A508-C402D8413363">ID2D1EffectImpl</a>



<a href="https://msdn.microsoft.com/9988aad6-0487-4f48-a05c-1dfb944f6ce7">ID2D1Factory::RegisterEffect</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

