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

# WofWimAddEntry function


## -description


Adds a single WIM data source to a volume such that files can be created on the volume which are stored within the WIM. 


## -parameters




### -param VolumeName [in]

The path to the volume upon which files residing in the WIM should be created.


### -param WimPath [in]

The path to the WIM file which should be used to provide data to files. 


### -param WimType [in]

The type of WIM. Can be <b>WIM_BOOT_OS_WIM</b> or <b>WIM_BOOT_NOT_OS_WIM</b>.  


### -param WimIndex [in]

Index of the image in the WIM which is applied.


### -param DataSourceId [out]

On successful return, contains the data source used to identify the entry.  This data source can be used to create new files with <a href="https://msdn.microsoft.com/E5BDD684-46AC-40C0-89FC-DFABBB6AB72C">WofSetFileDataLocation</a>. 


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn632437">FSCTL_ADD_OVERLAY</a>
 

 

