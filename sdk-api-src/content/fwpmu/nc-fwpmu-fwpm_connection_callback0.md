---
UID: NC:fwpmu.FWPM_CONNECTION_CALLBACK0
title: FWPM_CONNECTION_CALLBACK0 (fwpmu.h)
author: windows-sdk-content
description: Is used to add custom behavior to the connection object subscription process.
old-location: fwp\fwpm_connection_callback0.htm
tech.root: fwp
ms.assetid: 92aac379-6145-4556-a4cd-6a27fda4d910
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_CONNECTION_CALLBACK0, FWPM_CONNECTION_CALLBACK0 callback, FWPM_CONNECTION_CALLBACK0 callback function [Filtering], fwp.fwpm_connection_callback0, fwpmu/FWPM_CONNECTION_CALLBACK0
ms.topic: callback
f1_keywords: 
 - "fwpmu/FWPM_CONNECTION_CALLBACK0"
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - Fwpmu.h
api_name:
 - FWPM_CONNECTION_CALLBACK0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FWPM_CONNECTION_CALLBACK0 callback function


## -description


The <b>FWPM_CONNECTION_CALLBACK0</b> function is used to add custom behavior to the connection object subscription process.


## -parameters




### -param *context [in, out]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsubscribe0">FwpmConnectionSubscribe0</a> function.


### -param eventType [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type_">FWPM_CONNECTION_EVENT_TYPE</a></b>

The type of connection object change event.


### -param *connection [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_connection0_">FWPM_CONNECTION0</a>*</b>

The connection object change information.


## -returns



This callback function does not return a value.




## -remarks



Call <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsubscribe0">FwpmConnectionSubscribe0</a> to register this callback function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_connection0_">FWPM_CONNECTION0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type_">FWPM_CONNECTION_EVENT_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsubscribe0">FwpmConnectionSubscribe0</a>
 

 

