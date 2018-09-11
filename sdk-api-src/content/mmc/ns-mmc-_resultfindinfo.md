---
UID: NS:mmc._RESULTFINDINFO
title: "_RESULTFINDINFO"
author: windows-sdk-content
description: Used by the IResultOwnerData::FindItem method to support keyboard navigation in virtual lists in the result pane.
old-location: mmc\resultfindinfo.htm
tech.root: mmc
ms.assetid: e52c3437-45ac-4397-ab8f-70bc4d5f44f5
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: "*LPRESULTFINDINFO, LPRESULTFINDINFO, LPRESULTFINDINFO structure pointer [MMC], RESULTFINDINFO, RESULTFINDINFO structure [MMC], RFI_PARTIAL, RFI_WRAP, _RESULTFINDINFO, _slate_resultfindinfo, mmc.resultfindinfo, mmc/LPRESULTFINDINFO, mmc/RESULTFINDINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - Mmc.h
api_name:
 - RESULTFINDINFO
product: Windows
targetos: Windows
req.typenames: RESULTFINDINFO
req.redist: 
---

# _RESULTFINDINFO structure


## -description


The 
<b>RESULTFINDINFO</b> structure is used by the 
<a href="https://msdn.microsoft.com/839e6038-3f47-4192-b717-d81e4d9f202d">IResultOwnerData::FindItem</a> method to support keyboard navigation in virtual lists in the result pane.


## -struct-fields




### -field psz

Null-terminated string to match.


### -field nStart

Index at which to start search.


### -field dwOptions

One or both of the following flags:



#### RFI_PARTIAL

Match item names that begin with psz.



#### RFI_WRAP

Continue search at beginning of list if no match is found.


## -see-also




<a href="https://msdn.microsoft.com/839e6038-3f47-4192-b717-d81e4d9f202d">IResultOwnerData::FindItem</a>
 

 

