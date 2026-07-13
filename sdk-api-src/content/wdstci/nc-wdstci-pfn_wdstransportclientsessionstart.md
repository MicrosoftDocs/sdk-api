---
UID: NC:wdstci.PFN_WdsTransportClientSessionStart
title: PFN_WdsTransportClientSessionStart (wdstci.h)
description: The PFN_WdsTransportClientSessionStart callback is called at the start of a multicast session to indicate file size and other server side information about the file to the consumer. (PFN_WdsTransportClientSessionStart)
helpviewer_keywords: ["PFN_WdsTransportClientSessionStart","PFN_WdsTransportClientSessionStart callback","PFN_WdsTransportClientSessionStart callback function [Windows Deployment Services]","wds.pfn_wdstransportclientsessionstart","wdstci/PFN_WdsTransportClientSessionStart"]
old-location: wds\pfn_wdstransportclientsessionstart.htm
tech.root: wds
ms.assetid: 47a053e3-f457-4d0a-80a8-1b93d5e8688f
ms.date: 12/05/2018
ms.keywords: PFN_WdsTransportClientSessionStart, PFN_WdsTransportClientSessionStart callback, PFN_WdsTransportClientSessionStart callback function [Windows Deployment Services], wds.pfn_wdstransportclientsessionstart, wdstci/PFN_WdsTransportClientSessionStart
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_WdsTransportClientSessionStart
 - wdstci/PFN_WdsTransportClientSessionStart
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wdstci.h
api_name:
 - PFN_WdsTransportClientSessionStart
---

# PFN_WdsTransportClientSessionStart callback function


## -description

The PFN_WdsTransportClientSessionStart callback is called at the start of a multicast session to indicate file size and other server side information about the file to the consumer.

## -parameters

### -param hSessionKey [in]

The handle belonging to the session that is being started.

### -param pCallerData [in]

Pointer to the caller specific data for this session.  This data was specified in the call to WdsTransportClientStartSession.

### -param ullFileSize

#### - FileSize [in]

The total size of the file being transferred over multicast.

