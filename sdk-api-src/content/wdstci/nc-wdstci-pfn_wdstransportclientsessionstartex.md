---
UID: NC:wdstci.PFN_WdsTransportClientSessionStartEx
title: PFN_WdsTransportClientSessionStartEx
author: windows-driver-content
description: The PFN_WdsTransportClientSessionStart callback is called at the start of a multicast session to indicate file size and other server side information about the file to the consumer.
old-location: wds\pfn_wdstransportclientsessionstartex.htm
old-project: Wds
ms.assetid: 36970f1b-9dbf-421f-a078-3da3bbb050e8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: PFN_WdsTransportClientSessionStartEx, PFN_WdsTransportClientSessionStartEx callback function [Windows Deployment Services], wds.pfn_wdstransportclientsessionstartex, wdstci/PFN_WdsTransportClientSessionStartEx
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PXE_PROVIDER, *PPXE_PROVIDER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Wdstci.h
api_name:
-	PFN_WdsTransportClientSessionStartEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PFN_WdsTransportClientSessionStartEx callback


## -description


The PFN_WdsTransportClientSessionStart callback is called at the start of a multicast session to indicate file size and other server side information about the file to the consumer.


## -parameters




### -param hSessionKey [in]

The handle belonging to the session that is being started.


### -param pCallerData [in]

Pointer to the caller specific data for this session.  This data was specified in the call to WdsTransportClientStartSession.


### -param Info [in]

This parameter receives a pointer to a <a href="https://msdn.microsoft.com/21c96849-e122-4c4b-9d12-9f1c24908ac2">TRANSPORTCLIENT_SESSION_INFO</a> structure.


## -returns



This callback function does not return a value.



