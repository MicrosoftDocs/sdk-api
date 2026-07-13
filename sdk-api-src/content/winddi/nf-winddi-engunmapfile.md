---
UID: NF:winddi.EngUnmapFile
title: EngUnmapFile function (winddi.h)
description: The EngUnmapFile function unmaps the view of a file from system space.
helpviewer_keywords: ["EngUnmapFile","EngUnmapFile function [Display Devices]","display.engunmapfile","gdifncs_056f6d9c-2c92-4d88-b2b3-f016426d1aed.xml","winddi/EngUnmapFile"]
old-location: display\engunmapfile.htm
tech.root: display
ms.assetid: e98040c3-4817-470b-9f71-8ebf793fc9a8
ms.date: 12/05/2018
ms.keywords: EngUnmapFile, EngUnmapFile function [Display Devices], display.engunmapfile, gdifncs_056f6d9c-2c92-4d88-b2b3-f016426d1aed.xml, winddi/EngUnmapFile
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngUnmapFile
 - winddi/EngUnmapFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngUnmapFile
---

# EngUnmapFile function


## -description

The <b>EngUnmapFile</b> function unmaps the view of a file from <a href="/windows-hardware/drivers/">system space</a>.

## -parameters

### -param iFile [in]

Pointer to the identifier of the mapped file. This identifier was obtained in a prior call to <a href="/windows/desktop/api/winddi/nf-winddi-engmapfile">EngMapFile</a>.

## -returns

<b>EngUnmapFile</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engmapfile">EngMapFile</a>