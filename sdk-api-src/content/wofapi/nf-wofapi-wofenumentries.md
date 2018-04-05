---
UID: NF:wofapi.WofEnumEntries
title: WofEnumEntries function
author: windows-driver-content
description: Enumerates all the data sources from a specified provider for a specified volume.
old-location: fs\wofenumentries.htm
old-project: FileIO
ms.assetid: D6BCBFC1-C916-43E3-BB6A-E8EB6467850B
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: WofEnumEntries, WofEnumEntries function [Files], fs.wofenumentries, wofapi/WofEnumEntries
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
-	WofEnumEntries
product: Windows
targetos: Windows
req.lib: Wofutil.lib
req.dll: Wofutil.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WofEnumEntries function


## -description


Enumerates all the data sources from a specified provider for a specified volume. 


## -parameters




### -param VolumeName [in]

The volume name hosting the files for which the backing data sources are requested. 


### -param Provider [in]

Indicates which provider’s data sources are being requested.  Supported providers for this operation are: 
	  	

<table>
<tr>
<td>WOF_PROVIDER_WIM </td>
<td>Indicates that the function should return the WIM files which are providing data for placeholder files on the specified volume.</td>
</tr>
</table>
 


### -param EnumProc [in]

The callback function for each data source. The enumeration will stop          if <i>EnumProc</i> returns <b>FALSE</b>. 


### -param UserData [in, optional]

User defined data passed to <i>EnumProc</i>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn632440">FSCTL_ENUM_OVERLAY</a>
 

 

