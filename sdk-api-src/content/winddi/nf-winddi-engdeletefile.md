---
UID: NF:winddi.EngDeleteFile
title: EngDeleteFile function (winddi.h)
description: The EngDeleteFile function deletes a file.
helpviewer_keywords: ["EngDeleteFile","EngDeleteFile function [Display Devices]","display.engdeletefile","gdifncs_58a3395d-8a58-4a8a-b034-5dadc2dfc161.xml","winddi/EngDeleteFile"]
old-location: display\engdeletefile.htm
tech.root: display
ms.assetid: 2ed030cf-6d26-4bde-8d63-83fd6848ec0d
ms.date: 12/05/2018
ms.keywords: EngDeleteFile, EngDeleteFile function [Display Devices], display.engdeletefile, gdifncs_58a3395d-8a58-4a8a-b034-5dadc2dfc161.xml, winddi/EngDeleteFile
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
 - EngDeleteFile
 - winddi/EngDeleteFile
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
 - EngDeleteFile
---

# EngDeleteFile function


## -description

The <b>EngDeleteFile</b> function deletes a file.

## -parameters

### -param pwszFileName [in]

Pointer to a null-terminated string that contains the fully qualified name of the file to delete. An example of a fully qualified file name string is <i>L"\\??\\c:\\test.dat".</i>

## -returns

<b>EngDeleteFile</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engmapfile">EngMapFile</a>