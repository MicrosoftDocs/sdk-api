---
UID: NC:wdstci.PFN_WdsTransportClientSessionComplete
title: PFN_WdsTransportClientSessionComplete
author: windows-sdk-content
description: The PFN_WdsTransportClientSessionCompete callback is used by the client to indicate that no more callbacks will be sent to the consumer and that the session either completed successfully or encountered a non-recoverable error.
old-location: wds\pfn_wdstransportclientsessioncomplete.htm
tech.root: Wds
ms.assetid: 1c7b8137-bf74-486c-a90e-6becfec5ddc8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PFN_WdsTransportClientSessionComplete, PFN_WdsTransportClientSessionComplete callback, PFN_WdsTransportClientSessionComplete callback function [Windows Deployment Services], wds.pfn_wdstransportclientsessioncomplete, wdstci/PFN_WdsTransportClientSessionComplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: wdstci.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wdstci.h
api_name:
 - PFN_WdsTransportClientSessionComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_WdsTransportClientSessionComplete callback function


## -description


The PFN_WdsTransportClientSessionCompete callback is used by the client to indicate that no more callbacks will be sent to the consumer and that the session either completed successfully or encountered a non-recoverable error.


## -parameters




### -param hSessionKey [in]

The handle belonging to the session that is being started.


### -param pCallerData [in]

Pointer to the caller specific data for this session.  This data was specified in the call to <a href="https://msdn.microsoft.com/aa89899f-8f50-4617-84a1-4013412f0292">WdsTransportClientStartSession</a> function.


### -param dwError [in]

The overall status of the file transfer.  If the session succeeded, this value will be set to <b>ERROR_SUCCESS</b>.  If the session did not succeed, the error code for the session will be set.


## -returns



This callback function does not return a value.




## -remarks



This will be the last callback a consumer receives.  The consumer will always receive this callback, even if the session is canceled.  



