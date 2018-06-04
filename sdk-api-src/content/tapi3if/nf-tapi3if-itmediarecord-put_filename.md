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

# ITMediaRecord::put_FileName


## -description


The 
<b>put_FileName</b> method sets the name of the file to record.


## -parameters




### -param bstrFileName [in]

The <b>BSTR</b> representation of the file name.


#### - bAppendIfExists [in]

If this flag is set to <b>TRUE</b>, and a file with this name already exists, the new data will be appended to the file. If this flag is set to <b>FALSE</b>, and the file exists, the new data will overwrite the old data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/604b0128-1461-40f2-98fe-801dbb71e005">ITMediaRecord</a>



<a href="https://msdn.microsoft.com/fd97665c-ff9e-4621-baf9-7c0b603400c5">get_FileName</a>
 

 

