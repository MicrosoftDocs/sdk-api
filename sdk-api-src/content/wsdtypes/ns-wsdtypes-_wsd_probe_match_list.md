---
UID: NS:wsdtypes._WSD_PROBE_MATCH_LIST
title: "_WSD_PROBE_MATCH_LIST"
author: windows-sdk-content
description: Represents a node in a single-linked list of ProbeMatch message structures.
old-location: ncd\wsd_probe_match_list_struct.htm
old-project: wsdapi
ms.assetid: b7922300-1dc7-487f-b703-736cb0393f17
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSD_PROBE_MATCH_LIST, WSD_PROBE_MATCH_LIST structure, _WSD_PROBE_MATCH_LIST, ncd.wsd_probe_match_list_struct, wsdtypes/WSD_PROBE_MATCH_LIST
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
tech.root: 
req.typenames: WSD_PROBE_MATCH_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_PROBE_MATCH_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_PROBE_MATCH_LIST structure


## -description


Represents a node in a single-linked list of ProbeMatch message structures.


## -struct-fields




### -field Next

Reference to the next node in the linked list of <b>WSD_PROBE_MATCH_LIST</b> structures.


### -field Element

Reference to a <a href="https://msdn.microsoft.com/a30b11c8-df26-495d-87c3-aa67e400ec28">WSD_PROBE_MATCH</a> structure that contains the ProbeMatch message referenced by this node.


## -see-also




<a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe Message</a>



<a href="https://msdn.microsoft.com/58d3d016-ae29-4090-9b88-e1125db59c95">ProbeMatches Message</a>



<a href="https://msdn.microsoft.com/f84f7e77-ffe2-41af-a10f-a626466e9847">WSD_PROBE</a>



<a href="https://msdn.microsoft.com/a30b11c8-df26-495d-87c3-aa67e400ec28">WSD_PROBE_MATCH</a>



<a href="https://msdn.microsoft.com/41bf8dc2-903a-43d4-b63d-a34242d47288">WSD_PROBE_MATCHES</a>
 

 

