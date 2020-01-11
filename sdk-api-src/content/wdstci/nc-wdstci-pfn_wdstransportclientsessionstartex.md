---
UID: NC:wdstci.PFN_WdsTransportClientSessionStartEx
title: PFN_WdsTransportClientSessionStartEx (wdstci.h)
description: The PFN_WdsTransportClientSessionStart callback is called at the start of a multicast session to indicate file size and other server side information about the file to the consumer.
old-location: wds\pfn_wdstransportclientsessionstartex.htm
tech.root: wds
ms.assetid: 36970f1b-9dbf-421f-a078-3da3bbb050e8
ms.date: 12/05/2018
ms.keywords: PFN_WdsTransportClientSessionStartEx, PFN_WdsTransportClientSessionStartEx callback, PFN_WdsTransportClientSessionStartEx callback function [Windows Deployment Services], wds.pfn_wdstransportclientsessionstartex, wdstci/PFN_WdsTransportClientSessionStartEx
f1_keywords:
- wdstci/PFN_WdsTransportClientSessionStartEx
dev_langs:
- c++
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
- PFN_WdsTransportClientSessionStartEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PFN_WdsTransportClientSessionStartEx callback function


## -description


The PFN_WdsTransportClientSessionStart callback is called at the start of a multicast session to indicate file size and other server side information about the file to the consumer.


## -parameters




### -param hSessionKey [in]

The handle belonging to the session that is being started.


### -param pCallerData [in]

Pointer to the caller specific data for this session.  This data was specified in the call to WdsTransportClientStartSession.


### -param Info [in]

This parameter receives a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wdstci/ns-wdstci-transportclient_session_info">TRANSPORTCLIENT_SESSION_INFO</a> structure.


## -returns



This callback function does not return a value.



