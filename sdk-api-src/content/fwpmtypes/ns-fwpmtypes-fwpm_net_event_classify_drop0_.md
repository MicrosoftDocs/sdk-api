---
UID: NS:fwpmtypes.FWPM_NET_EVENT_CLASSIFY_DROP0_
title: FWPM_NET_EVENT_CLASSIFY_DROP0_
author: windows-sdk-content
description: Contains information that describes a layer drop failure.
old-location: fwp\fwpm_net_event_classify_drop0.htm
tech.root: fwp
ms.assetid: 9688ff75-292f-44f2-b3ed-41a9dd1ef918
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: FWPM_NET_EVENT_CLASSIFY_DROP0, FWPM_NET_EVENT_CLASSIFY_DROP0 structure [Filtering], FWPM_NET_EVENT_CLASSIFY_DROP0_, fwp.fwpm_net_event_classify_drop0, fwpmtypes/FWPM_NET_EVENT_CLASSIFY_DROP0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - FWPM_NET_EVENT_CLASSIFY_DROP0
product: Windows
targetos: Windows
req.typenames: FWPM_NET_EVENT_CLASSIFY_DROP0
req.redist: 
---

# FWPM_NET_EVENT_CLASSIFY_DROP0_ structure


## -description


The <b>FWPM_NET_EVENT_CLASSIFY_DROP0</b> structure contains information that describes a layer drop  failure.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_CLASSIFY_DROP0</b> is the specific implementation of FWPM_NET_EVENT_CLASSIFY_DROP used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/2bc38e75-450e-4ad7-8954-ff339ae769f5">FWPM_NET_EVENT_CLASSIFY_DROP1</a> is available. For Windows 8, <a href="https://msdn.microsoft.com/1e018d6c-ed56-43f9-90b3-f2af42861617">FWPM_NET_EVENT_CLASSIFY_DROP2</a> is available. </div><div> </div>

## -struct-fields




### -field filterId

A LUID identifying the filter where the failure occurred.


### -field layerId

Indicates the identifier of the filtering layer where the failure occurred.  For more information, see <a href="https://msdn.microsoft.com/3b2daef1-558b-4e3a-a98a-f4dfa80a29c0">Filtering Layer Identifiers</a>.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

