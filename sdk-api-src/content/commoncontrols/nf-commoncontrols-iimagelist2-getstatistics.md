---
UID: NF:commoncontrols.IImageList2.GetStatistics
title: IImageList2::GetStatistics (commoncontrols.h)
description: Gets an image list statistics structure.
helpviewer_keywords: ["GetStatistics","GetStatistics method [Windows Controls]","GetStatistics method [Windows Controls]","IImageList2 interface","IImageList2 interface [Windows Controls]","GetStatistics method","IImageList2.GetStatistics","IImageList2::GetStatistics","_shell_IImageList2_GetStatistics","_shell_IImageList2_GetStatistics_cpp","commoncontrols/IImageList2::GetStatistics","controls.IImageList2_GetStatistics","controls._shell_IImageList2_GetStatistics"]
old-location: controls\IImageList2_GetStatistics.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\getstatistics.htm
ms.date: 12/05/2018
ms.keywords: GetStatistics, GetStatistics method [Windows Controls], GetStatistics method [Windows Controls],IImageList2 interface, IImageList2 interface [Windows Controls],GetStatistics method, IImageList2.GetStatistics, IImageList2::GetStatistics, _shell_IImageList2_GetStatistics, _shell_IImageList2_GetStatistics_cpp, commoncontrols/IImageList2::GetStatistics, controls.IImageList2_GetStatistics, controls._shell_IImageList2_GetStatistics
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Commoncontrols.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IImageList2::GetStatistics
 - commoncontrols/IImageList2::GetStatistics
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList2.GetStatistics
---

# IImageList2::GetStatistics


## -description

Gets an image list statistics structure.

## -parameters

### -param pils [in, out]

Type: <b><a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imageliststats">IMAGELISTSTATS</a>*</b>

A pointer to the <a href="/windows/desktop/api/commoncontrols/ns-commoncontrols-imageliststats">IMAGELISTSTATS</a> structure.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.