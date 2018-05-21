---
UID: NF:wofapi.WofWimRemoveEntry
title: WofWimRemoveEntry function
author: windows-driver-content
description: Removes a single WIM data source from backing files on a volume.
old-location: fs\wofwimremoveentry.htm
old-project: FileIO
ms.assetid: B376EDF7-8C46-4C8B-900E-0DC79699EC1E
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: WofWimRemoveEntry, WofWimRemoveEntry function [Files], fs.wofwimremoveentry, wofapi/WofWimRemoveEntry
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
-	WofWimRemoveEntry
product: Windows
targetos: Windows
req.lib: Wofutil.lib
req.dll: Wofutil.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WofWimRemoveEntry function


## -description


Removes a single WIM data source from backing files on a volume. 


## -parameters




### -param VolumeName [in]

The volume name which contained files whose data was provided by the WIM.


### -param DataSourceId [in]

Identifes the WIM entry.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the volume currently has files whose data is derived from the WIM file, the data for those files will become permanently inaccessible. It is good practice to remove any files referring to the WIM file prior to removing the data source from a volume.  Once all data sources for a WIM file have been removed, the WIM file itself can be renamed or deleted.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn632442">FSCTL_REMOVE_OVERLAY</a>
 

 

