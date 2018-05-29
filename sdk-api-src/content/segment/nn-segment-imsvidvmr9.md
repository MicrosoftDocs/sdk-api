---
UID: NN:segment.IMSVidVMR9
title: IMSVidVMR9
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005. The IMSVidVMR9 interface represents the Video Mixing Renderer Filter 9 (VMR-9) within the Video Control filter graph. The MSVidVMR9 object exposes this interface.
old-location: mstv\imsvidvmr9.htm
old-project: mstv
ms.assetid: c96f91d4-fc6c-4422-8fc9-ea5fed10bd80
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidVMR9, IMSVidVMR9 interface [Microsoft TV Technologies], IMSVidVMR9 interface [Microsoft TV Technologies],described, IMSVidVMR9Interface, mstv.imsvidvmr9, segment/IMSVidVMR9
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidVMR9
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidVMR9 interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IMSVidVMR9</b> interface represents the <a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a> (VMR-9) within the Video Control filter graph. The <a href="https://msdn.microsoft.com/b8c07511-2665-43d6-b7ce-d478ee1af69c">MSVidVMR9</a> object exposes this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidVMR9</b> interface inherits from <a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer</a>. <b>IMSVidVMR9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidVMR9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd19c85b-21dc-410a-9fa1-99e1f1d8be30">get_Allocator</a>
</td>
<td align="left" width="63%">
Retrieves the application's custom allocator-presenter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46ea07af-be29-4621-96cb-f3c17be12f85">get_Allocator_ID</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the application's custom allocator-presenter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d2d10fe-39c2-4ee1-a5c5-5624b2fbc2ef">get_SuppressEffects</a>
</td>
<td align="left" width="63%">
Queries whether the Video Control configures the system for optimal video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e51ed2a-7516-4621-9ecb-0e645c6d416c">put_SuppressEffects</a>
</td>
<td align="left" width="63%">
Specifies whether the Video Control configures the system for optimal video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f654adac-12b6-47c7-99d4-0612b1532df4">SetAllocator</a>
</td>
<td align="left" width="63%">
Sets a custom allocator-presenter for the VMR-9.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidVMR9)</code>.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

