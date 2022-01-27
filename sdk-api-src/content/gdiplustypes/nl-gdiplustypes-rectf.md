---
UID: NL:gdiplustypes.RectF
title: RectF (gdiplustypes.h)
description: A RectF object stores the upper-left corner, width, and height of a rectangle.
helpviewer_keywords: ["RectF","RectF class [GDI+]","RectF class [GDI+]","described","_gdiplus_CLASS_RectF_Class","gdiplus._gdiplus_CLASS_RectF_Class","gdiplustypes/RectF"]
old-location: gdiplus\_gdiplus_CLASS_RectF_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectf.htm
ms.date: 12/05/2018
ms.keywords: RectF, RectF class [GDI+], RectF class [GDI+],described, _gdiplus_CLASS_RectF_Class, gdiplus._gdiplus_CLASS_RectF_Class, gdiplustypes/RectF
req.header: gdiplustypes.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RectF
 - gdiplustypes/RectF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplustypes.h
api_name:
 - RectF
---

# RectF class


## -description

A <b>RectF</b> object stores the upper-left corner, width, and height of a rectangle.

<h3><a id="constructors"></a>Constructors</h3>The <b>RectF</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-rectf(inconstpointf__inconstsizef_)">RectF::RectF()</a>
</td>
<td align="left" width="63%">
Creates a <b>RectF</b> object and initializes the 
			<b>X</b> and 
			<b>Y</b> data members to zero. This is the default constructor.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-rectf(inconstpointf__inconstsizef_)">RectF::RectF(PointF&,SizeF&)</a>
</td>
<td align="left" width="63%">
Creates a <b>RectF</b> object by using a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> object to initialize the 
			<b>X</b> and 
			<b>Y</b> data members and uses a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a> object to initialize the 
			<b>Width</b> and 
			<b>Height</b> data members of this rectangle.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-rectf(inreal_inreal_inreal_inreal)">RectF::RectF(REAL,REAL,REAL,REAL)</a>
</td>
<td align="left" width="63%">
Creates a <b>RectF</b> object by using four integers to initialize the 
			<b>X</b>, 
			<b>Y</b>, 
			<b>Width</b>, and 
			<b>Height</b> data members.

</td>
</tr>
</table> 


## -remarks

The upper-left corner of the rectangle is located at (
				<i>x</i>, 
				<i>y</i>). The size of the rectangle is measured by 
				<i>width</i> and 
				<i>height</i>. There are methods for high-level functionality, such as moving, resizing, and performing or testing interactions with other rectangles.
