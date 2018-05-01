---
UID: NF:fltuser.FilterVolumeInstanceFindClose
title: FilterVolumeInstanceFindClose function
author: windows-driver-content
description: The FilterVolumeInstanceFindClose function closes the specified volume instance search handle. FilterVolumeInstanceFindFirst and FilterVolumeInstanceFindNext use this search handle to locate instances on a volume.
old-location: ifsk\filtervolumeinstancefindclose.htm
old-project: ifsk
ms.assetid: 4c56bcea-c027-4607-8531-da971e43e763
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: FilterVolumeInstanceFindClose, FilterVolumeInstanceFindClose function [Installable File System Drivers], FltWin32ApiRef_5cdcef76-2a6d-4d64-9af6-09b050073573.xml, fltuser/FilterVolumeInstanceFindClose, ifsk.filtervolumeinstancefindclose
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fltuser.h
req.include-header: Fltuser.h
req.target-type: Universal
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
req.typenames: FILTERED_DATA_SOURCES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	FltLib.dll
api_name:
-	FilterVolumeInstanceFindClose
product: Windows
targetos: Windows
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
req.product: Internet Explorer 5
---

# FilterVolumeInstanceFindClose function


## -description


The <b>FilterVolumeInstanceFindClose</b> function closes the specified volume instance search handle. <a href="https://msdn.microsoft.com/library/windows/hardware/ff541541">FilterVolumeInstanceFindFirst</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff541551">FilterVolumeInstanceFindNext</a> use this search handle to locate instances on a volume. 


## -parameters




### -param hVolumeInstanceFind [in]

Volume instance search handle to close. This handle must have been opened by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff541541">FilterVolumeInstanceFindFirst</a>. 


## -returns



<b>FilterVolumeInstanceFindClose</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



After the <b>FilterVolumeInstanceFindClose</b> function is called, the handle specified by the <i>hVolumeInstanceFind</i> parameter cannot be used in subsequent calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff541551">FilterVolumeInstanceFindNext</a> or <b>FilterVolumeInstanceFindClose</b>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541541">FilterVolumeInstanceFindFirst</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541551">FilterVolumeInstanceFindNext</a>
 

 

