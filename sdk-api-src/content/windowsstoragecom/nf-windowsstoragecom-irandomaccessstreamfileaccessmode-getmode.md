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

# IRandomAccessStreamFileAccessMode::GetMode


## -description


Retrieves the file access mode that was used when the <a href="https://msdn.microsoft.com/128318b6-ddfb-44d0-9fcb-80410ad284bf">StorageFile.OpenAsync</a> method was called to open the random-access byte stream.


## -parameters




### -param fileAccessMode [out]

The file access mode that was used when the <a href="https://msdn.microsoft.com/128318b6-ddfb-44d0-9fcb-80410ad284bf">StorageFile.OpenAsync</a> method was called to open the random-access byte stream. Cast this value as a <a href="https://msdn.microsoft.com/2905de68-84f9-4cc1-9389-8ec611b1eece">Windows::Storage::FileAccessMode</a> enumeration value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/20A538B5-ACD6-4BD9-9CDC-3F2CCDCAF251">IRandomAccessStreamFileAccessMode</a>



<a href="https://msdn.microsoft.com/128318b6-ddfb-44d0-9fcb-80410ad284bf">StorageFile.OpenAsync</a>



<a href="https://msdn.microsoft.com/2905de68-84f9-4cc1-9389-8ec611b1eece">Windows::Storage::FileAccessMode</a>
 

 

