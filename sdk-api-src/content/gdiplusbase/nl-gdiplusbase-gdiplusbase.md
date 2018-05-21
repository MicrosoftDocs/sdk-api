---
UID: NL:gdiplusbase.GdiplusBase
title: GdiplusBase
author: windows-driver-content
description: The GdiplusBase class provides memory allocation and deallocation for GDI+ objects. GdiplusBase serves as a base class for all other GDI+ classes, so you never need to create an instance of GdiplusBase.
old-location: gdiplus\_gdiplus_CLASS_GdiplusBase_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\gdiplusbase.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GdiplusBase, GdiplusBase class [GDI+], GdiplusBase class [GDI+],described, _gdiplus_CLASS_GdiplusBase_Class, gdiplus._gdiplus_CLASS_GdiplusBase_Class, gdiplusbase/GdiplusBase
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
req.header: gdiplusbase.h
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
req.typenames: KnownGamingPrivileges
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	gdiplusbase.h
api_name:
-	GdiplusBase
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# GdiplusBase class


## -description


The <b>GdiplusBase</b> class provides memory allocation and deallocation for GDI+ objects. <b>GdiplusBase</b> serves as a base class for all other GDI+ classes, so you never need to create an instance of <b>GdiplusBase</b>.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">GdiplusBase</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>GdiplusBase</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b489f6d6-bc04-4234-8f77-b48dce1f2fe6">GdiplusBase::operator delete</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b489f6d6-bc04-4234-8f77-b48dce1f2fe6">GdiplusBase::operator delete</a> method deallocates memory for one GDI+ object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6adfeb24-5124-4b6a-99ab-cb53f8cd0738">GdiplusBase::operator delete[]</a>
</td>
<td align="left" width="63%">
The 
		xref rid="_gdiplus_CLASS_GdiplusBase_operator_delete_bracket_in_pVoid_" qualify="0"/&gt; 
		method deallocates memory for an array of GDI+ 
		objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/360c68bd-6fef-47de-9213-8ddb93d21095">GdiplusBase::operator new</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/360c68bd-6fef-47de-9213-8ddb93d21095">GdiplusBase::operator new</a> method allocates memory for one GDI+ object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70e6de3a-4eef-4f6b-9fb0-35ddc51c44c3">GdiplusBase::operator new[]</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/70e6de3a-4eef-4f6b-9fb0-35ddc51c44c3">GdiplusBase::operator new[]</a> method allocates memory for an array of GDI+ objects.

</td>
</tr>
</table> 

