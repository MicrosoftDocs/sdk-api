---
UID: NS:shlobj_core.tagDATABLOCKHEADER
title: DATABLOCK_HEADER (shlobj_core.h)
author: windows-sdk-content
description: Serves as the header for some of the extra data structures used by IShellLinkDataList.
old-location: shell\DATABLOCK_HEADER_str.htm
tech.root: shell
ms.assetid: 06de45c2-8cb5-45e3-9639-d4625c24d27b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDATABLOCK_HEADER, *LPDBLIST, DATABLOCK_HEADER, DATABLOCK_HEADER structure [Windows Shell], LPDATABLOCK_HEADER, LPDATABLOCK_HEADER structure pointer [Windows Shell], LPDBLIST, LPDBLIST structure pointer [Windows Shell], _win32_DATABLOCK_HEADER_str, shell.DATABLOCK_HEADER_str, shlobj_core/DATABLOCK_HEADER, shlobj_core/LPDATABLOCK_HEADER, shlobj_core/LPDBLIST, tagDATABLOCKHEADER"
ms.topic: struct
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - DATABLOCK_HEADER
product: Windows
targetos: Windows
req.typenames: DATABLOCK_HEADER, *LPDATABLOCK_HEADER, *LPDBLIST
req.redist: 
ms.custom: 19H1
---

# DATABLOCK_HEADER structure


## -description


Serves as the header for some of the extra data structures used by <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist">IShellLinkDataList</a>.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the extra data block.


### -field dwSignature

Type: <b>DWORD</b>

A signature that identifies the type of data block that follows the header.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_darwin_link">EXP_DARWIN_LINK</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_console_props">NT_CONSOLE_PROPS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_fe_console_props">NT_FE_CONSOLE_PROPS</a>
 

 

