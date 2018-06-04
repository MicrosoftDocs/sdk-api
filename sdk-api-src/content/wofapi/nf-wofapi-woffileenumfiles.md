---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

