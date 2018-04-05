---
UID: NF:wofapi.WofFileEnumFiles
title: WofFileEnumFiles function
author: windows-driver-content
description: Enumerates all of the files which are compressed with a specified compression algorithm on a specified volume.
old-location: fs\woffileenumfiles.htm
old-project: FileIO
ms.assetid: 0B3CD8A2-AF4C-4438-B284-03AAA81DE436
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: WofFileEnumFiles, WofFileEnumFiles function [Files], fs.woffileenumfiles, wofapi/WofFileEnumFiles
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
req.typenames: WNV_REDIRECT_PARAM, *PWNV_REDIRECT_PARAM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	wofutil.dll
api_name:
-	WofFileEnumFiles
product: Windows
targetos: Windows
req.lib: Wofutil.lib
req.dll: Wofutil.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WofFileEnumFiles function


## -description


Enumerates all of the files which are compressed with a specified compression algorithm on a specified volume.


## -parameters




### -param VolumeName [in]

A full path to the volume containing the files to enumerate. 


### -param Algorithm [in]

The compression algorithm to enumerate.  For a list of valid compression algorithms, see <a href="https://msdn.microsoft.com/84FC5525-43BC-436C-AADC-C58882D48C1F">WOF_FILE_COMPRESSION_INFO_V1</a>.  If this value is MAX_ULONG, files compressed with any supported compression algorithm will be returned.


### -param EnumProc [in]

The callback function for each data source. The enumeration will stop if <i>EnumProc</i> returns FALSE. 


### -param UserData [in, optional]

User defined data passed to <i>EnumProc</i>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn632439">FSCTL_ENUM_EXTERNAL_BACKING</a>
 

 

