---
UID: NF:tapi.lineConfigProvider
title: lineConfigProvider function
author: windows-sdk-content
description: The lineConfigProvider function causes a service provider to display its configuration dialog box.
old-location: tapi2\lineconfigprovider.htm
tech.root: tapi
ms.assetid: 3149b353-6380-4fa9-a6ef-cf4566aaff58
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "_tapi2_lineconfigprovider, lineConfigProvider, lineConfigProvider function [TAPI 2.2], tapi/lineConfigProvider, tapi2.lineconfigprovider"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tapi.h
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineConfigProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

