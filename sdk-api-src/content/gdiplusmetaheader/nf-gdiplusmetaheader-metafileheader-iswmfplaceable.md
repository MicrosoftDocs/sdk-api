---
UID: NF:gdiplusmetaheader.MetafileHeader.IsWmfPlaceable
title: MetafileHeader::IsWmfPlaceable
author: windows-sdk-content
description: The MetafileHeader::IsWmfPlaceable method determines whether the associated metafile is a placeable metafile.
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_IsWmfPlaceable_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\iswmfplaceable.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IsWmfPlaceable, IsWmfPlaceable method [GDI+], IsWmfPlaceable method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],IsWmfPlaceable method, MetafileHeader.IsWmfPlaceable, MetafileHeader::IsWmfPlaceable, _gdiplus_CLASS_MetafileHeader_IsWmfPlaceable_, gdiplus._gdiplus_CLASS_MetafileHeader_IsWmfPlaceable_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusmetaheader.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Gdiplus.dll
api_name:
 - MetafileHeader.IsWmfPlaceable
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# MetafileHeader::IsWmfPlaceable


## -description


The <b>MetafileHeader::IsWmfPlaceable</b> method determines whether the associated metafile is a placeable metafile.


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the associated metafile is a placeable metafile, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



Placeable metafiles are .wmf files that contain a preheader preceding the metafile header. The preheader contains additional information for the metafile header of the metafile.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a> object from a .wmf file and gets the metafile header of the metafile. The code then determines whether the metafile is a placeable metafile.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
MetafileHeader metaHeader;
Metafile::GetMetafileHeader(L"sampleMetafile.wmf", &amp;metaHeader);

if(metaHeader.IsWmfPlaceable() == TRUE)
{
   // The associated metafile is a placeable metafile.
}
				</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/985c412f-10ba-4ce9-b0e1-89f5b643c22a">EmfType</a>



<a href="https://msdn.microsoft.com/79b8df1b-6fc5-455b-9d08-57d64bf6bffa">Loading and Displaying Metafiles</a>



<a href="https://msdn.microsoft.com/4ea75699-c3c7-481e-b369-3bdc600b9713">MetafileHeader</a>



<a href="https://msdn.microsoft.com/a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077">Metafiles</a>
 

 

