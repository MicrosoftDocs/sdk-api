---
UID: NS:mmiscapi.tagDRVCONFIGINFO
title: DRVCONFIGINFO (mmiscapi.h)
description: Contains the registry key and value names associated with the installable driver.
helpviewer_keywords: ["*LPDRVCONFIGINFO","*NPDRVCONFIGINFO","*PDRVCONFIGINFO","DRVCONFIGINFO","DRVCONFIGINFO structure [Windows Multimedia]","_win32_DRVCONFIGINFO_str","mmsystem/DRVCONFIGINFO","multimedia.drvconfiginfo","tagDRVCONFIGINFO"]
old-location: multimedia\drvconfiginfo.htm
tech.root: Multimedia
ms.assetid: 34451e1c-0748-48c7-9e5e-877a0c531a07
ms.date: 12/05/2018
ms.keywords: '*LPDRVCONFIGINFO, *NPDRVCONFIGINFO, *PDRVCONFIGINFO, DRVCONFIGINFO, DRVCONFIGINFO structure [Windows Multimedia], _win32_DRVCONFIGINFO_str, mmsystem/DRVCONFIGINFO, multimedia.drvconfiginfo, tagDRVCONFIGINFO'
req.header: mmiscapi.h
req.include-header: Mmiscapi.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
targetos: Windows
req.typenames: DRVCONFIGINFO, *PDRVCONFIGINFO, *NPDRVCONFIGINFO, *LPDRVCONFIGINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDRVCONFIGINFO
 - mmiscapi/tagDRVCONFIGINFO
 - PDRVCONFIGINFO
 - mmiscapi/PDRVCONFIGINFO
 - DRVCONFIGINFO
 - mmiscapi/DRVCONFIGINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmsystem.h
api_name:
 - DRVCONFIGINFO
---

# DRVCONFIGINFO structure


## -description

Contains the registry key and value names associated with the installable driver.

## -struct-fields

### -field dwDCISize

Size of the structure, in bytes.

### -field lpszDCISectionName

Address of a null-terminated, wide-character string specifying the name of the registry key associated with the driver.

### -field lpszDCIAliasName

Address of a null-terminated, wide-character string specifying the name of the registry value associated with the driver.

## -see-also

Installable Driver Structures



Installable Drivers

