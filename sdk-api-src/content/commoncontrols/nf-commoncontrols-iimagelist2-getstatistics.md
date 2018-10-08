---
UID: NF:commoncontrols.IImageList2.GetStatistics
title: IImageList2::GetStatistics
author: windows-sdk-content
description: Gets an image list statistics structure.
old-location: controls\IImageList2_GetStatistics.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\getstatistics.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetStatistics, GetStatistics method [Windows Controls], GetStatistics method [Windows Controls],IImageList2 interface, IImageList2 interface [Windows Controls],GetStatistics method, IImageList2.GetStatistics, IImageList2::GetStatistics, _shell_IImageList2_GetStatistics, _shell_IImageList2_GetStatistics_cpp, commoncontrols/IImageList2::GetStatistics, controls.IImageList2_GetStatistics, controls._shell_IImageList2_GetStatistics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList2.GetStatistics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageList2::GetStatistics


## -description


Gets an image list statistics structure.


## -parameters




### -param pils [in, out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb761397(v=VS.85).aspx">IMAGELISTSTATS</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb761397(v=VS.85).aspx">IMAGELISTSTATS</a> structure.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



