---
UID: NF:wofapi.WofWimEnumFiles
title: WofWimEnumFiles function
author: windows-sdk-content
description: Enumerates all of the files which are being backed by a specified WIM data source on a specified volume.
old-location: fs\wofwimenumfiles.htm
tech.root: fileio
ms.assetid: D95F344F-762F-4F3C-ADAE-0A20BAE448F2
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: WofWimEnumFiles, WofWimEnumFiles function [Files], fs.wofwimenumfiles, wofapi/WofWimEnumFiles
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Wofutil.lib
req.dll: Wofutil.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wofutil.dll
api_name:
 - WofWimEnumFiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WofWimEnumFiles function


## -description


Enumerates all of the files which are being backed by a specified WIM data source on a specified volume. 


## -parameters




### -param VolumeName [in]

The path to the volume which hosts WIM-backed files.


### -param DataSourceId [in]

Identifier used to identify the WIM entry. 


### -param EnumProc [in]

The callback function for file provided by the WIM entry.


### -param UserData [in, optional]

Optional user defined data passed to <i>EnumProc</i>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



