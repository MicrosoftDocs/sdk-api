---
UID: NF:cfapi.CfGetPlaceholderStateFromFindData
title: CfGetPlaceholderStateFromFindData function (cfapi.h)
author: windows-sdk-content
description: Gets a set of placeholder states based on the WIN32_FIND_DATA structure.
old-location: cloudapi\cfgetplaceholderstatefromfinddata.htm
tech.root: cfApi
ms.assetid: 1A8104BC-E9D1-4846-B91F-4CBEDB1FC542
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CfGetPlaceholderStateFromFindData, CfGetPlaceholderStateFromFindData function, cfapi/CfGetPlaceholderStateFromFindData, cloudApi.cfgetplaceholderstatefromfinddata
ms.topic: function
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfGetPlaceholderStateFromFindData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CfGetPlaceholderStateFromFindData function


## -description


Gets a set of placeholder states based on the WIN32_FIND_DATA structure.


## -parameters




### -param FindData [in]

The find data information on the file.


## -returns



Can include <a href="https://msdn.microsoft.com/5E814458-2045-4CFD-90AC-F1F53DEB4FD0">CF_PLACEHOLDER_STATE</a>; The placeholder state.




## -remarks



The WIN32_FIND_DATA structure is obtained from the Win32 <a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a>/<a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a> functions.



