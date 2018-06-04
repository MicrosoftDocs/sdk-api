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
 

 

