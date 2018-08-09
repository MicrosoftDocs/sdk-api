---
UID: NF:cscobj.IEnumOfflineFilesSettings.Skip
title: IEnumOfflineFilesSettings::Skip
author: windows-sdk-content
description: Skips over the next specified number of elements in the enumeration.
old-location: of\ienumofflinefilessettings_skip.htm
old-project: offlinefiles
ms.assetid: 8b84fcef-f4e3-4e23-b254-dd21f145c1ba
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumOfflineFilesSettings interface [Offline Files],Skip method, IEnumOfflineFilesSettings.Skip, IEnumOfflineFilesSettings::Skip, Skip, Skip method [Offline Files], Skip method [Offline Files],IEnumOfflineFilesSettings interface, cscobj/IEnumOfflineFilesSettings::Skip, of.ienumofflinefilessettings_skip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IEnumOfflineFilesSettings.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IEnumOfflineFilesSettings::Skip


## -description


Skips over the next specified number of elements in the enumeration.


## -parameters




### -param celt [in]

Number of elements to be skipped.


## -returns



Returns <b>S_OK</b> if the number of elements skipped is <i>celt</i>; S_FALSE if a number less than <i>celt</i> is skipped; or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/2d0e45d5-5559-4c2e-9c20-4e5b84b5fbbd">IEnumOfflineFilesSettings</a>
 

 

