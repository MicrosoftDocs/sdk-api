---
UID: NS:wsdtypes._WSD_PROBE_MATCHES
title: "_WSD_PROBE_MATCHES"
author: windows-sdk-content
description: Represents a ProbeMatches message.
old-location: ncd\wsd_probe_matches_struct.htm
tech.root: WsdApi
ms.assetid: 41bf8dc2-903a-43d4-b63d-a34242d47288
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WSD_PROBE_MATCHES, WSD_PROBE_MATCHES structure, _WSD_PROBE_MATCHES, ncd.wsd_probe_matches_struct, wsdtypes/WSD_PROBE_MATCHES
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_PROBE_MATCHES
product: Windows
targetos: Windows
req.typenames: WSD_PROBE_MATCHES
req.redist: 
---

# _WSD_PROBE_MATCHES structure


## -description


Represents a  <a href="https://msdn.microsoft.com/58d3d016-ae29-4090-9b88-e1125db59c95">ProbeMatches</a> message.


## -struct-fields




### -field ProbeMatch

Reference to a <a href="https://msdn.microsoft.com/b7922300-1dc7-487f-b703-736cb0393f17">WSD_PROBE_MATCH_LIST</a> structure that contains the list of matches to the <a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe</a> message.


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.


## -see-also




<a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe Message</a>



<a href="https://msdn.microsoft.com/58d3d016-ae29-4090-9b88-e1125db59c95">ProbeMatches Message</a>



<a href="https://msdn.microsoft.com/f84f7e77-ffe2-41af-a10f-a626466e9847">WSD_PROBE</a>



<a href="https://msdn.microsoft.com/a30b11c8-df26-495d-87c3-aa67e400ec28">WSD_PROBE_MATCH</a>



<a href="https://msdn.microsoft.com/b7922300-1dc7-487f-b703-736cb0393f17">WSD_PROBE_MATCH_LIST</a>
 

 

