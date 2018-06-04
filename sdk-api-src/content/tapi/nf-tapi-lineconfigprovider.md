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

# lineConfigProvider function


## -description


The 
<b>lineConfigProvider</b> function causes a service provider to display its configuration dialog box.


## -parameters




### -param hwndOwner

Handle to a window to which the configuration dialog box (displayed by 
<a href="https://msdn.microsoft.com/b0fa2a9e-bc8b-4364-9442-2091f2366107">TSPI_providerConfig</a>) is attached. Can be <b>NULL</b> to indicate that any window created during the function should have no owner window.


### -param dwPermanentProviderID

Permanent provider identifier of the service provider to be configured.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INIFILECORRUPT, LINEERR_NOMEM, LINEERR_INVALPARAM, LINEERR_OPERATIONFAILED.




## -remarks



This is basically a straight pass-through to 
<a href="https://msdn.microsoft.com/b0fa2a9e-bc8b-4364-9442-2091f2366107">TSPI_providerConfig</a>.




## -see-also




<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

