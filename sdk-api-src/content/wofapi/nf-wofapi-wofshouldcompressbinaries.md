---
UID: NF:wofapi.WofShouldCompressBinaries
title: WofShouldCompressBinaries function
author: windows-sdk-content
description: Indicates whether compression should be used on a particular volume, and if so, which compression algorithm should be used.
old-location: fs\wofshouldcompressbinaries.htm
old-project: fileio
ms.assetid: C7A1D76A-2535-46BB-A55B-D1E15A079FF4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WofShouldCompressBinaries, WofShouldCompressBinaries function [Files], fs.wofshouldcompressbinaries, wofapi/WofShouldCompressBinaries
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wofapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
tech.root: 
req.typenames: WNV_REDIRECT_PARAM, *PWNV_REDIRECT_PARAM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wofutil.dll
api_name:
 - WofShouldCompressBinaries
product: Windows
targetos: Windows
req.lib: Wofutil.lib
req.dll: Wofutil.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WofShouldCompressBinaries function


## -description


Indicates whether compression should be used on a particular volume, and if so, which compression algorithm should be used. 



## -parameters




### -param Volume [in]

Specifies the path to the volume whose compression state is desired. 


### -param Algorithm [out]

Points to a ULONG value. If the function returns TRUE, indicating compression is desired, this value will contain the algorithm that should be used for this volume. 



## -returns



If binaries on this volume should be compressed, the return value is TRUE; otherwise it is FALSE. This function will return FALSE if the system does not support compression on the specified volume. 





