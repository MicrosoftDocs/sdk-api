---
UID: NF:winnls.FILEMUIINFO_GET_MAIN_TYPEID
title: FILEMUIINFO_GET_MAIN_TYPEID macro (winnls.h)
author: windows-sdk-content
description: Gets the main module types array element associated with the type identifier size and offset in a FILEMUIINFO structure. The information is provided in the dwTypeIDMainSize and dwTypeIDMainOffset members of the structure.
old-location: intl\filemuiinfo_get_main_typeid.htm
tech.root: Intl
ms.assetid: 0102b364-ffc7-48a0-a7d1-5a64fba6428e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FILEMUIINFO_GET_MAIN_TYPEID, FILEMUIINFO_GET_MAIN_TYPEID macro [Internationalization for Windows Applications], _win32_FILEMUIINFO_GET_MAIN_TYPEID, intl.filemuiinfo_get_main_typeid, winnls/FILEMUIINFO_GET_MAIN_TYPEID
ms.topic: macro
f1_keywords:
- winnls/FILEMUIINFO_GET_MAIN_TYPEID
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- Winnls.h
api_name:
- FILEMUIINFO_GET_MAIN_TYPEID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FILEMUIINFO_GET_MAIN_TYPEID macro


## -description


Gets the main module types array element associated with the type identifier size and offset in a <a href="https://docs.microsoft.com/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure. The information is provided in the <b>dwTypeIDMainSize</b> and <b>dwTypeIDMainOffset</b> members of the structure.


## -parameters




### -param pInfo

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure.


### -param iType

Index of the array element.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/multilingual-user-interface-macros">Multilingual User Interface Macros</a>
 

 

