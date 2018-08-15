---
UID: NL:gdiplusmetaheader.MetafileHeader
title: MetafileHeader
author: windows-sdk-content
description: A MetafileHeader object stores properties of an associated metafile.
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheader.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: MetafileHeader, MetafileHeader class [GDI+], MetafileHeader class [GDI+],described, _gdiplus_CLASS_MetafileHeader_Class, gdiplus._gdiplus_CLASS_MetafileHeader_Class, gdiplusmetaheader/MetafileHeader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: gdiplusmetaheader.h
req.include-header: 
req.redist: 
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
req.typenames: 
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
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
<a href="https://msdn.microsoft.com/0f8385cb-c9a1-4667-ab0d-22d0b5dda1fd">MetafileHeader::GetBounds</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0f8385cb-c9a1-4667-ab0d-22d0b5dda1fd">MetafileHeader::GetBounds</a> method gets the bounding rectangle for the associated metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2e3620e-53c7-40ee-bcd9-061ad0ad1503">MetafileHeader::GetDpiX</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d2e3620e-53c7-40ee-bcd9-061ad0ad1503">MetafileHeader::GetDpiX</a> method gets the horizontal dots per inch of the associated metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6c43b4b-d5f9-4d1d-afba-fc59b238a73e">MetafileHeader::GetDpiY</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c6c43b4b-d5f9-4d1d-afba-fc59b238a73e">MetafileHeader::GetDpiY</a> method gets the vertical dots per inch of the associated metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13f70025-46a3-41e8-8cc9-aa01f1b978a3">MetafileHeader::GetEmfHeader</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/13f70025-46a3-41e8-8cc9-aa01f1b978a3">MetafileHeader::GetEmfHeader</a> method gets an <a href="https://msdn.microsoft.com/48cacd83-8123-476c-af78-11ad41285c3e">ENHMETAHEADER3</a> structure that contains properties of the associated metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d04d621c-a84b-4d74-a308-da391425f658">MetafileHeader::GetEmfPlusFlags</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d04d621c-a84b-4d74-a308-da391425f658">MetafileHeader::GetEmfPlusFlags</a> method gets a flag that indicates whether the associated metafile was recorded against a video display device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff1a84fe-511b-4744-8076-c74532df29ab">MetafileHeader::GetMetafileSize</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ff1a84fe-511b-4744-8076-c74532df29ab">MetafileHeader::GetMetafileSize</a> method gets the size, in bytes, of the metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42acdd2c-b87d-455a-83c0-0630bd552c45">MetafileHeader::GetType</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/42acdd2c-b87d-455a-83c0-0630bd552c45">MetafileHeader::GetType</a> method gets the type of the associated metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a0dac87-d667-4c9a-ae15-8183baf14e91">MetafileHeader::GetVersion</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/8a0dac87-d667-4c9a-ae15-8183baf14e91">MetafileHeader::GetVersion</a> method gets the version of the metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/026f0e5c-165f-4115-8320-83b6e1b47377">MetafileHeader::GetWmfHeader</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/026f0e5c-165f-4115-8320-83b6e1b47377">MetafileHeader::GetWmfHeader</a> method gets a <a href="https://msdn.microsoft.com/3ad5be24-9558-442e-8c77-dd6a7d33c208">METAHEADER</a> structure that contains properties of the associated metafile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2acf40d-1c8f-418a-8598-4254f3929096">MetafileHeader::IsDisplay</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c2acf40d-1c8f-418a-8598-4254f3929096">MetafileHeader::IsDisplay</a> method determines whether the associated metafile was recorded against a video display device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2c1470d-1efb-48ef-8046-d710331423e2">MetafileHeader::IsEmf</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b2c1470d-1efb-48ef-8046-d710331423e2">MetafileHeader::IsEmf</a> method determines whether the associated metafile is in the EMF format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/901c2f13-44a1-4432-8e35-b3708615d492">MetafileHeader::IsEmfOrEmfPlus</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/901c2f13-44a1-4432-8e35-b3708615d492">MetafileHeader::IsEmfOrEmfPlus</a> method determines whether the associated metafile is in either the EMF or EMF+ format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1403ea16-d470-49ef-982a-34f747323006">MetafileHeader::IsEmfPlus</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/1403ea16-d470-49ef-982a-34f747323006">MetafileHeader::IsEmfPlus</a> method determines whether the associated metafile is in the EMF+ format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37e87bcd-fcb7-4f90-9d8e-e74cb61d17b1">MetafileHeader::IsEmfPlusDual</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/37e87bcd-fcb7-4f90-9d8e-e74cb61d17b1">MetafileHeader::IsEmfPlusDual</a> method determines whether the associated metafile is in the EMF+ Dual format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4dd24c66-2a72-41bb-9a7e-46f493763be1">MetafileHeader::IsEmfPlusOnly</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/4dd24c66-2a72-41bb-9a7e-46f493763be1">MetafileHeader::IsEmfPlusOnly</a> method determines whether the associated metafile is in the EMF+ Only format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8cd3ae8-25ee-4d40-aeb9-43b7a2de4d62">MetafileHeader::IsWmf</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a8cd3ae8-25ee-4d40-aeb9-43b7a2de4d62">MetafileHeader::IsWmf</a> method determines whether the associated metafile is in the WMF format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e8fed26-8877-4bfe-a52e-4b365c7f2c2b">MetafileHeader::IsWmfPlaceable</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/8e8fed26-8877-4bfe-a52e-4b365c7f2c2b">MetafileHeader::IsWmfPlaceable</a> method determines whether the associated metafile is a placeable metafile.

</td>
</tr>
</table> 


## -remarks



Metafiles provide a device-independent and application-independent way to share pictures. They contain records that describe a sequence of graphics APIs to invoke in a particular order with their associated graphics data. Metafiles can be recorded by an application and later played back by that application or by another one to reproduce a particular picture. They can also be used to send content to a print spooler. Enhanced metafiles support the ability to provide both Windows GDI+ and Windows Graphics Device Interface (GDI) descriptions of the same picture so that both GDI+ and down-level GDI applications can render it.



