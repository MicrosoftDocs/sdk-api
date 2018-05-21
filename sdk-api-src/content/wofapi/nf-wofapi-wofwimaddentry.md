---
UID: NF:wofapi.WofWimAddEntry
title: WofWimAddEntry function
author: windows-driver-content
description: Adds a single WIM data source to a volume such that files can be created on the volume which are stored within the WIM.
old-location: fs\wofwimaddentry.htm
old-project: FileIO
ms.assetid: 53CE16AE-E14D-4E51-87E2-DDF88D5CE806
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: WofWimAddEntry, WofWimAddEntry function [Files], fs.wofwimaddentry, wofapi/WofWimAddEntry
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
-	WofWimAddEntry
product: Windows
targetos: Windows
req.lib: Wofutil.lib
req.dll: Wofutil.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

