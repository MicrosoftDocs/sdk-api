---
UID: NF:rdpencomapi.IRDPSRAPIPerfCounterLoggingManager.CreateLogger
title: IRDPSRAPIPerfCounterLoggingManager::CreateLogger (rdpencomapi.h)
description: Creates a new IRDPSRAPIPerfCounterLogger object.
old-location: rdp\irdpsrapiperfcounterloggingmanager_createlogger.htm
tech.root: rdp
ms.assetid: 24C57AE8-208B-4254-B5B1-8AB77E2D4044
ms.date: 12/05/2018
ms.keywords: CreateLogger, CreateLogger method [RDP], CreateLogger method [RDP],IRDPSRAPIPerfCounterLoggingManager interface, IRDPSRAPIPerfCounterLoggingManager interface [RDP],CreateLogger method, IRDPSRAPIPerfCounterLoggingManager.CreateLogger, IRDPSRAPIPerfCounterLoggingManager::CreateLogger, rdp.irdpsrapiperfcounterloggingmanager_createlogger, rdpencomapi/IRDPSRAPIPerfCounterLoggingManager::CreateLogger
ms.topic: method
f1_keywords:
- rdpencomapi/IRDPSRAPIPerfCounterLoggingManager.CreateLogger
dev_langs:
- c++
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- RdpEncom.dll
api_name:
- IRDPSRAPIPerfCounterLoggingManager.CreateLogger
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRDPSRAPIPerfCounterLoggingManager::CreateLogger


## -description


Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiperfcounterlogger">IRDPSRAPIPerfCounterLogger</a> object.


## -parameters




### -param bstrCounterName [in]

The name of the counter.


### -param ppLogger [out]

An <a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiperfcounterlogger">IRDPSRAPIPerfCounterLogger</a> interface pointer.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiperfcounterloggingmanager">IRDPSRAPIPerfCounterLoggingManager</a>
 

 

