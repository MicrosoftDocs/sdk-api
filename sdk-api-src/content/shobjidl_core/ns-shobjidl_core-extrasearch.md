---
UID: NS:shobjidl_core.EXTRASEARCH
title: EXTRASEARCH (shobjidl_core.h)
author: windows-sdk-content
description: Used by an IEnumExtraSearch enumerator object to return information on the search objects supported by a Shell Folder object.
old-location: shell\EXTRASEARCH.htm
tech.root: shell
ms.assetid: d930a00b-3084-4da7-8915-0bebdb33df9b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPEXTRASEARCH, EXTRASEARCH, EXTRASEARCH structure [Windows Shell], LPEXTRASEARCH, LPEXTRASEARCH structure pointer [Windows Shell], _win32_EXTRASEARCH, shell.EXTRASEARCH, shobjidl_core/EXTRASEARCH, shobjidl_core/LPEXTRASEARCH"
ms.topic: struct
f1_keywords: 
 - "shobjidl_core/EXTRASEARCH"
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - EXTRASEARCH
targetos: Windows
req.typenames: EXTRASEARCH, *LPEXTRASEARCH
req.redist: 
ms.custom: 19H1
---

# EXTRASEARCH structure


## -description


Used by an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch">IEnumExtraSearch</a> enumerator object to return information on the search objects supported by a Shell Folder object.


## -struct-fields




### -field guidSearch

Type: <b>GUID</b>

A search object's GUID.


### -field wszFriendlyName

Type: <b>WCHAR[80]</b>

A Unicode string containing the search object's friendly name. It will be used to identify the search engine on the Search Assistant menu.


### -field wszUrl

Type: <b>WCHAR[2084]</b>

The URL that will be displayed in the search pane.

