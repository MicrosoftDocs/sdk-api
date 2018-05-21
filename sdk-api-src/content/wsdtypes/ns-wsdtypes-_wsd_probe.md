---
UID: NS:wsdtypes._WSD_PROBE
title: "_WSD_PROBE"
author: windows-driver-content
description: Represents a Probe message.
old-location: ncd\wsd_probe_struct.htm
old-project: WsdApi
ms.assetid: f84f7e77-ffe2-41af-a10f-a626466e9847
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: WSD_PROBE, WSD_PROBE structure, _WSD_PROBE, ncd.wsd_probe_struct, wsdtypes/WSD_PROBE
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.idl: Wsdhost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSD_PROBE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WsdTypes.h
api_name:
-	WSD_PROBE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_PROBE structure


## -description


Represents a <a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe</a> message.


## -struct-fields




### -field Types

Reference to a <a href="https://msdn.microsoft.com/f573365d-100f-4df9-b1af-a484680436eb">WSD_NAME_LIST</a> structure that contains a list of WS-Discovery Types.


### -field Scopes

Reference to a <a href="https://msdn.microsoft.com/3415fef0-dbf4-4ece-bad0-6cd6831404db">WSD_SCOPES</a> structure that contains a list of WS-Discovery Scopes.


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.


## -see-also




<a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe Message</a>



<a href="https://msdn.microsoft.com/58d3d016-ae29-4090-9b88-e1125db59c95">ProbeMatches Message</a>



<a href="https://msdn.microsoft.com/a30b11c8-df26-495d-87c3-aa67e400ec28">WSD_PROBE_MATCH</a>



<a href="https://msdn.microsoft.com/41bf8dc2-903a-43d4-b63d-a34242d47288">WSD_PROBE_MATCHES</a>



<a href="https://msdn.microsoft.com/b7922300-1dc7-487f-b703-736cb0393f17">WSD_PROBE_MATCH_LIST</a>
 

 

