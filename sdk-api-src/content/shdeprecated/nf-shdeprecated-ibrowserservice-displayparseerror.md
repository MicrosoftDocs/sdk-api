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

# IBrowserService::DisplayParseError


## -description


Deprecated. Displays a URL that failed to be successfully parsed by <a href="https://msdn.microsoft.com/02f5a6cb-2f90-4613-80cd-1e8a47bb32c2">IBrowserService::IEParseDisplayName</a>.


## -parameters




### -param hres [in]

Type: <b>HRESULT</b>

An <b>HRESULT</b> returned by <a href="https://msdn.microsoft.com/02f5a6cb-2f90-4613-80cd-1e8a47bb32c2">IBrowserService::IEParseDisplayName</a>. If this parameter is a success code, E_OUTOFMEMORY, or HRESULT_FROM_WIN32(ERROR_CANCELLED), this method does nothing.


### -param pwszPath [in]

Type: <b>LPCWSTR</b>


          A pointer to a buffer containing the URL that failed to parse. This method displays the failed URL in an error dialog box.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        The <b>HRESULT</b> returned by <a href="https://msdn.microsoft.com/02f5a6cb-2f90-4613-80cd-1e8a47bb32c2">IBrowserService::IEParseDisplayName</a> can be passed to <b>IBrowserService::DisplayParseError</b> without first checking for success or failure.
      



