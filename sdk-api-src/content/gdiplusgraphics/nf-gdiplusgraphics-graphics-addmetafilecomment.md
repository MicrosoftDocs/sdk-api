---
UID: NF:gdiplusgraphics.Graphics.AddMetafileComment
title: Graphics::AddMetafileComment
author: windows-sdk-content
description: The Graphics::AddMetafileComment method adds a text comment to an existing metafile.
old-location: gdiplus\_gdiplus_CLASS_Graphics_AddMetafileComment_data_sizeData_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\addmetafilecomment.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: AddMetafileComment, AddMetafileComment method [GDI+], AddMetafileComment method [GDI+],Graphics class, Graphics class [GDI+],AddMetafileComment method, Graphics.AddMetafileComment, Graphics::AddMetafileComment, _gdiplus_CLASS_Graphics_AddMetafileComment_data_sizeData_, gdiplus._gdiplus_CLASS_Graphics_AddMetafileComment_data_sizeData_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusgraphics.h
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
 - Graphics.AddMetafileComment
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::AddMetafileComment


## -description


The <b>Graphics::AddMetafileComment</b> method adds a text comment to an existing metafile.


## -parameters




### -param data [in]

Type: <b>const BYTE*</b>

Pointer to a buffer that contains the comment. 


### -param sizeData [in]

Type: <b>UINT</b>

Integer that specifies the number of bytes in the value of the 
					<i>data</i> parameter. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/library/ms533831(v=VS.85).aspx">Loading and Displaying Metafiles</a>



<a href="https://msdn.microsoft.com/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/library/ms534480(v=VS.85).aspx">MetafileHeader</a>



<a href="https://msdn.microsoft.com/library/ms536391(v=VS.85).aspx">Metafiles</a>
 

 

