---
UID: NS:wsdtypes._WSD_PROBE_MATCH
title: "_WSD_PROBE_MATCH"
author: windows-sdk-content
description: Represents a ProbeMatch message.
old-location: ncd\wsd_probe_match_struct.htm
old-project: wsdapi
ms.assetid: a30b11c8-df26-495d-87c3-aa67e400ec28
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSD_PROBE_MATCH, WSD_PROBE_MATCH structure, _WSD_PROBE_MATCH, ncd.wsd_probe_match_struct, wsdtypes/WSD_PROBE_MATCH
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
req.typenames: WSD_PROBE_MATCH
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_PROBE_MATCH
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_PROBE_MATCH structure


## -description


Represents a ProbeMatch message.


## -struct-fields




### -field EndpointReference

Reference to a <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a> structure that specifies the matching endpoint.


### -field Types

Reference to a <a href="https://msdn.microsoft.com/f573365d-100f-4df9-b1af-a484680436eb">WSD_NAME_LIST</a> structure that contains a list of WS-Discovery Types.


### -field Scopes

Reference to a <a href="https://msdn.microsoft.com/3415fef0-dbf4-4ece-bad0-6cd6831404db">WSD_SCOPES</a> structure that contains a list of WS-Discovery Scopes.


### -field XAddrs

Reference to a <a href="https://msdn.microsoft.com/86d77741-39c3-44bd-b072-d2d4eb99e488">WSD_URI_LIST</a> structure that contains a list of WS-Discovery XAddrs.


### -field MetadataVersion

The metadata version of this message.


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.


## -see-also




<a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe Message</a>



<a href="https://msdn.microsoft.com/58d3d016-ae29-4090-9b88-e1125db59c95">ProbeMatches Message</a>



<a href="https://msdn.microsoft.com/f84f7e77-ffe2-41af-a10f-a626466e9847">WSD_PROBE</a>



<a href="https://msdn.microsoft.com/41bf8dc2-903a-43d4-b63d-a34242d47288">WSD_PROBE_MATCHES</a>



<a href="https://msdn.microsoft.com/b7922300-1dc7-487f-b703-736cb0393f17">WSD_PROBE_MATCH_LIST</a>
 

 

