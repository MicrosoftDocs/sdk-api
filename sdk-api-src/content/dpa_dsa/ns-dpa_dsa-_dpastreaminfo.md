---
UID: NS:dpa_dsa._DPASTREAMINFO
title: "_DPASTREAMINFO"
author: windows-sdk-content
description: Contains a stream item used by the PFNDPASTREAM callback function.
old-location: controls\DPASTREAMINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\dpastreaminfo.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: DPASTREAMINFO, DPASTREAMINFO structure [Windows Controls], _DPASTREAMINFO, _win32_DPASTREAMINFO, _win32_DPASTREAMINFO_cpp, controls.DPASTREAMINFO, controls._win32_DPASTREAMINFO, dpa_dsa/DPASTREAMINFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - dpa_dsa.h
api_name:
 - DPASTREAMINFO
product: Windows
targetos: Windows
req.typenames: DPASTREAMINFO
req.redist: 
---

# _DPASTREAMINFO structure


## -description


Contains a stream item used by the <a href="https://msdn.microsoft.com/b5910ac3-9066-49d8-8cb3-796de22428d3">PFNDPASTREAM</a> callback function. 


## -struct-fields




### -field iPos

Type: <b>int</b>

An index of the item in the DPA. 


### -field pvItem

Type: <b>void*</b>

A void pointer to the item data. 

