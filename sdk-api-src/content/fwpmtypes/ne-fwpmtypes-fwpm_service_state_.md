---
UID: NE:fwpmtypes.FWPM_SERVICE_STATE_
title: FWPM_SERVICE_STATE_
author: windows-sdk-content
description: Specifies the current state of the filter engine.
old-location: fwp\fwpm_service_state.htm
tech.root: FWP
ms.assetid: 80a3695a-71ac-4c8b-897e-80c4231ad570
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: FWPM_SERVICE_RUNNING, FWPM_SERVICE_START_PENDING, FWPM_SERVICE_STATE, FWPM_SERVICE_STATE enumeration [Filtering], FWPM_SERVICE_STATE_, FWPM_SERVICE_STATE_MAX, FWPM_SERVICE_STOPPED, FWPM_SERVICE_STOP_PENDING, fwp.fwpm_service_state, fwpmtypes/FWPM_SERVICE_RUNNING, fwpmtypes/FWPM_SERVICE_START_PENDING, fwpmtypes/FWPM_SERVICE_STATE, fwpmtypes/FWPM_SERVICE_STATE_MAX, fwpmtypes/FWPM_SERVICE_STOPPED, fwpmtypes/FWPM_SERVICE_STOP_PENDING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
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
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_SERVICE_STATE
product: Windows
targetos: Windows
req.typenames: FWPM_SERVICE_STATE
req.redist: 
---

# FWPM_SERVICE_STATE_ enumeration


## -description


The <b>FWPM_SERVICE_STATE</b> enumeration specifies the current state of the filter engine.


## -enum-fields




### -field FWPM_SERVICE_STOPPED

The filter engine is not running.


### -field FWPM_SERVICE_START_PENDING

The filter engine is starting.


### -field FWPM_SERVICE_STOP_PENDING

The filter engine is stopping.


### -field FWPM_SERVICE_RUNNING

The filter engine is running.


### -field FWPM_SERVICE_STATE_MAX

Maximum value for testing purposes.


## -see-also




<a href="https://msdn.microsoft.com/39029412-18ce-426a-a79d-cf25ff0dfe0d">Windows Filtering Platform API Enumerated Types</a>
 

 

