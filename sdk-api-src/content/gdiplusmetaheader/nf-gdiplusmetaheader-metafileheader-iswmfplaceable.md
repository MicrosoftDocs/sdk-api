---
UID: NF:gdiplusmetaheader.MetafileHeader.IsWmfPlaceable
title: MetafileHeader::IsWmfPlaceable
author: windows-sdk-content
description: The MetafileHeader::IsWmfPlaceable method determines whether the associated metafile is a placeable metafile.
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_IsWmfPlaceable_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\iswmfplaceable.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IsWmfPlaceable, IsWmfPlaceable method [GDI+], IsWmfPlaceable method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],IsWmfPlaceable method, MetafileHeader.IsWmfPlaceable, MetafileHeader::IsWmfPlaceable, _gdiplus_CLASS_MetafileHeader_IsWmfPlaceable_, gdiplus._gdiplus_CLASS_MetafileHeader_IsWmfPlaceable_
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
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
req.typenames: 
req.redist: 
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
						<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a> object from a .wmf file and gets the metafile header of the metafile. The code then determines whether the metafile is a placeable metafile.

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




<a href="https://msdn.microsoft.com/en-us/library/ms534115(v=VS.85).aspx">EmfType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533831(v=VS.85).aspx">Loading and Displaying Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534480(v=VS.85).aspx">MetafileHeader</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536391(v=VS.85).aspx">Metafiles</a>
 

 

