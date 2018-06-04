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

# AmsiScanBuffer function


## -description


Scans a buffer-full of content for malware.


## -parameters




### -param amsiContext [in]

The handle of type HAMSICONTEXT that was initially received from <a href="https://msdn.microsoft.com/946FC79C-556C-404E-A559-323AA69B3EC6">AmsiInitialize</a>.


### -param buffer [in]

The buffer from which to read the data to be scanned.


### -param length [in]

The length, in bytes, of the data to be read from <i>buffer</i>.


### -param contentName [in]

The filename, URL, unique script ID, or similar of the content being scanned.


### -param amsiSession

TBD


### -param result [out]

The result of the scan. See <a href="https://msdn.microsoft.com/3D7C74E3-BB09-4C53-930D-72D352374151">AMSI_RESULT</a>.

An app should use <a href="https://msdn.microsoft.com/1C7B48D9-FD1C-48B5-AA7F-0ED7382E106A">AmsiResultIsMalware</a> to determine whether the content should be blocked.


#### - session [in, optional]

If multiple scan requests are to be correlated within a session, set <i>session</i> to the handle of type HAMSISESSION that was initially received from <a href="https://msdn.microsoft.com/588C9003-8689-4D1C-BDFB-386E60BAECD5">AmsiOpenSession</a>. Otherwise, set <i>session</i> to <b>nullptr</b>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3D7C74E3-BB09-4C53-930D-72D352374151">AMSI_RESULT</a>



<a href="https://msdn.microsoft.com/946FC79C-556C-404E-A559-323AA69B3EC6">AmsiInitialize</a>



<a href="https://msdn.microsoft.com/588C9003-8689-4D1C-BDFB-386E60BAECD5">AmsiOpenSession</a>



<a href="https://msdn.microsoft.com/1C7B48D9-FD1C-48B5-AA7F-0ED7382E106A">AmsiResultIsMalware</a>
 

 

