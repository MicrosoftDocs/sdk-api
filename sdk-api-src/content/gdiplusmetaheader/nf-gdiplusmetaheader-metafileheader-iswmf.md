---
UID: NF:gdiplusmetaheader.MetafileHeader.IsWmf
title: MetafileHeader::IsWmf (gdiplusmetaheader.h)
description: The MetafileHeader::IsWmf method determines whether the associated metafile is in the WMF format.
helpviewer_keywords: ["IsWmf","IsWmf method [GDI+]","IsWmf method [GDI+]","MetafileHeader class","MetafileHeader class [GDI+]","IsWmf method","MetafileHeader.IsWmf","MetafileHeader::IsWmf","_gdiplus_CLASS_MetafileHeader_IsWmf_","gdiplus._gdiplus_CLASS_MetafileHeader_IsWmf_"]
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_IsWmf_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\iswmf.htm
ms.date: 12/05/2018
ms.keywords: IsWmf, IsWmf method [GDI+], IsWmf method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],IsWmf method, MetafileHeader.IsWmf, MetafileHeader::IsWmf, _gdiplus_CLASS_MetafileHeader_IsWmf_, gdiplus._gdiplus_CLASS_MetafileHeader_IsWmf_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - MetafileHeader::IsWmf
 - gdiplusmetaheader/MetafileHeader::IsWmf
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - MetafileHeader.IsWmf
---

# MetafileHeader::IsWmf


## -description

The <b>MetafileHeader::IsWmf</b> method determines whether the associated metafile is in the WMF format.



## -returns

Type: <b>BOOL</b>

If the associated metafile is in the WMF format, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>. In particular, this method returns <b>FALSE</b> if the associated metafile is in the EMF or EMF+ format.

