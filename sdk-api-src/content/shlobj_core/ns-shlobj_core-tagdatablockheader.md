---
UID: NS:shlobj_core.tagDATABLOCKHEADER
title: tagDATABLOCKHEADER
author: windows-driver-content
description: Serves as the header for some of the extra data structures used by IShellLinkDataList.
old-location: shell\DATABLOCK_HEADER_str.htm
old-project: shell
ms.assetid: 06de45c2-8cb5-45e3-9639-d4625c24d27b
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*LPDATABLOCK_HEADER, *LPDBLIST, DATABLOCK_HEADER, DATABLOCK_HEADER structure [Windows Shell], LPDATABLOCK_HEADER, LPDATABLOCK_HEADER structure pointer [Windows Shell], LPDBLIST, LPDBLIST structure pointer [Windows Shell], _win32_DATABLOCK_HEADER_str, shell.DATABLOCK_HEADER_str, shlobj_core/DATABLOCK_HEADER, shlobj_core/LPDATABLOCK_HEADER, shlobj_core/LPDBLIST, tagDATABLOCKHEADER"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DATABLOCK_HEADER, *LPDATABLOCK_HEADER, *LPDBLIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	shlobj_core.h
api_name:
-	DATABLOCK_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# tagDATABLOCKHEADER structure


## -description


Serves as the header for some of the extra data structures used by <a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the extra data block.


### -field dwSignature

Type: <b>DWORD</b>

A signature that identifies the type of data block that follows the header.


## -see-also




<a href="https://msdn.microsoft.com/016c539e-6035-4752-99b6-71e2d7199bf0">EXP_DARWIN_LINK</a>



<a href="https://msdn.microsoft.com/02542cd4-be8f-45c0-ad0f-e1e39a45f5de">NT_CONSOLE_PROPS</a>



<a href="https://msdn.microsoft.com/2f22676d-2b46-4a94-9517-64d1caeead43">NT_FE_CONSOLE_PROPS</a>
 

 

