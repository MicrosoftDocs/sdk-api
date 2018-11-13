---
UID: NL:gdiplusmetaheader.MetafileHeader
title: MetafileHeader
author: windows-sdk-content
description: A MetafileHeader object stores properties of an associated metafile.
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheader.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: MetafileHeader, MetafileHeader class [GDI+], MetafileHeader class [GDI+],described, _gdiplus_CLASS_MetafileHeader_Class, gdiplus._gdiplus_CLASS_MetafileHeader_Class, gdiplusmetaheader/MetafileHeader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: gdiplusmetaheader.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplusmetaheader.h
api_name:
 - MetafileHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MetafileHeader class


## -description


A <b>MetafileHeader</b> object stores properties of an associated metafile.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">MetafileHeader</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>MetafileHeader</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535105(v=VS.85).aspx">MetafileHeader::GetBounds</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535105(v=VS.85).aspx">MetafileHeader::GetBounds</a> method gets the bounding rectangle for the associated metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535106(v=VS.85).aspx">MetafileHeader::GetDpiX</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535106(v=VS.85).aspx">MetafileHeader::GetDpiX</a> method gets the horizontal dots per inch of the associated metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535107(v=VS.85).aspx">MetafileHeader::GetDpiY</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535107(v=VS.85).aspx">MetafileHeader::GetDpiY</a> method gets the vertical dots per inch of the associated metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535108(v=VS.85).aspx">MetafileHeader::GetEmfHeader</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535108(v=VS.85).aspx">MetafileHeader::GetEmfHeader</a> method gets an <a href="https://msdn.microsoft.com/en-us/library/ms534065(v=VS.85).aspx">ENHMETAHEADER3</a> structure that contains properties of the associated metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535109(v=VS.85).aspx">MetafileHeader::GetEmfPlusFlags</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535109(v=VS.85).aspx">MetafileHeader::GetEmfPlusFlags</a> method gets a flag that indicates whether the associated metafile was recorded against a video display device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535110(v=VS.85).aspx">MetafileHeader::GetMetafileSize</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535110(v=VS.85).aspx">MetafileHeader::GetMetafileSize</a> method gets the size, in bytes, of the metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535112(v=VS.85).aspx">MetafileHeader::GetType</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535112(v=VS.85).aspx">MetafileHeader::GetType</a> method gets the type of the associated metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535113(v=VS.85).aspx">MetafileHeader::GetVersion</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535113(v=VS.85).aspx">MetafileHeader::GetVersion</a> method gets the version of the metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535114(v=VS.85).aspx">MetafileHeader::GetWmfHeader</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535114(v=VS.85).aspx">MetafileHeader::GetWmfHeader</a> method gets a <a href="https://msdn.microsoft.com/3ad5be24-9558-442e-8c77-dd6a7d33c208">METAHEADER</a> structure that contains properties of the associated metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535115(v=VS.85).aspx">MetafileHeader::IsDisplay</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535115(v=VS.85).aspx">MetafileHeader::IsDisplay</a> method determines whether the associated metafile was recorded against a video display device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535116(v=VS.85).aspx">MetafileHeader::IsEmf</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535116(v=VS.85).aspx">MetafileHeader::IsEmf</a> method determines whether the associated metafile is in the EMF format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535117(v=VS.85).aspx">MetafileHeader::IsEmfOrEmfPlus</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535117(v=VS.85).aspx">MetafileHeader::IsEmfOrEmfPlus</a> method determines whether the associated metafile is in either the EMF or EMF+ format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535118(v=VS.85).aspx">MetafileHeader::IsEmfPlus</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535118(v=VS.85).aspx">MetafileHeader::IsEmfPlus</a> method determines whether the associated metafile is in the EMF+ format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535119(v=VS.85).aspx">MetafileHeader::IsEmfPlusDual</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535119(v=VS.85).aspx">MetafileHeader::IsEmfPlusDual</a> method determines whether the associated metafile is in the EMF+ Dual format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535264(v=VS.85).aspx">MetafileHeader::IsEmfPlusOnly</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535264(v=VS.85).aspx">MetafileHeader::IsEmfPlusOnly</a> method determines whether the associated metafile is in the EMF+ Only format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535265(v=VS.85).aspx">MetafileHeader::IsWmf</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535265(v=VS.85).aspx">MetafileHeader::IsWmf</a> method determines whether the associated metafile is in the WMF format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535266(v=VS.85).aspx">MetafileHeader::IsWmfPlaceable</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535266(v=VS.85).aspx">MetafileHeader::IsWmfPlaceable</a> method determines whether the associated metafile is a placeable metafile.

</td>
</tr>
</table> 


## -remarks



Metafiles provide a device-independent and application-independent way to share pictures. They contain records that describe a sequence of graphics APIs to invoke in a particular order with their associated graphics data. Metafiles can be recorded by an application and later played back by that application or by another one to reproduce a particular picture. They can also be used to send content to a print spooler. Enhanced metafiles support the ability to provide both Windows GDI+ and Windows Graphics Device Interface (GDI) descriptions of the same picture so that both GDI+ and down-level GDI applications can render it.



