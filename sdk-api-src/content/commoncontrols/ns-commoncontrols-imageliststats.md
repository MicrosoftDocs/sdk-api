---
UID: NS:commoncontrols.tagIMAGELISTSTATS
title: IMAGELISTSTATS (commoncontrols.h)
description: Contains image list statistics. Used by GetStatistics.
helpviewer_keywords: ["IMAGELISTSTATS","IMAGELISTSTATS structure [Windows Controls]","_shell_IMAGELISTSTATS","_shell_IMAGELISTSTATS_cpp","commoncontrols/IMAGELISTSTATS","controls.IMAGELISTSTATS","controls._shell_IMAGELISTSTATS"]
old-location: controls\IMAGELISTSTATS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\structures\imageliststats.htm
ms.date: 12/05/2018
ms.keywords: IMAGELISTSTATS, IMAGELISTSTATS structure [Windows Controls], _shell_IMAGELISTSTATS, _shell_IMAGELISTSTATS_cpp, commoncontrols/IMAGELISTSTATS, controls.IMAGELISTSTATS, controls._shell_IMAGELISTSTATS
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IMAGELISTSTATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagIMAGELISTSTATS
 - commoncontrols/tagIMAGELISTSTATS
 - IMAGELISTSTATS
 - commoncontrols/IMAGELISTSTATS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commoncontrols.h
api_name:
 - IMAGELISTSTATS
---

# IMAGELISTSTATS structure


## -description

Contains image list statistics. Used by <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist2-getstatistics">GetStatistics</a>.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The image list size.

### -field cAlloc

Type: <b>int</b>

The number of images allocated.

### -field cUsed

Type: <b>int</b>

The number of images in use.

### -field cStandby

Type: <b>int</b>

The number of standby images.