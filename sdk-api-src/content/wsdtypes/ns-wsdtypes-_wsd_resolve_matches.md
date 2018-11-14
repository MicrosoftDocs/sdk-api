---
UID: NS:wsdtypes._WSD_RESOLVE_MATCHES
title: "_WSD_RESOLVE_MATCHES"
author: windows-sdk-content
description: Represents a ResolveMatches message.
old-location: ncd\wsd_resolve_matches.htm
tech.root: WsdApi
ms.assetid: a6094069-af17-4921-b2c3-4ec89cbbb6f6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WSD_RESOLVE_MATCHES, WSD_RESOLVE_MATCHES structure, _WSD_RESOLVE_MATCHES, ncd.wsd_resolve_matches, wsdtypes/WSD_RESOLVE_MATCHES
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
 - WSD_RESOLVE_MATCHES
product: Windows
targetos: Windows
req.typenames: WSD_RESOLVE_MATCHES
req.redist: 
---

# _WSD_RESOLVE_MATCHES structure


## -description


Represents a <a href="https://msdn.microsoft.com/b963bd2a-47cb-4f8d-8272-a586e6d6a047">ResolveMatches</a> message.


## -struct-fields




### -field ResolveMatch

Reference to a <a href="https://msdn.microsoft.com/eabcc3af-282c-4299-8061-6cddf14eca6b">WSD_RESOLVE_MATCH</a> structure that contains a child ResolveMatch message.


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.


## -see-also




<a href="https://msdn.microsoft.com/b963bd2a-47cb-4f8d-8272-a586e6d6a047">ResolveMatches Message</a>



<a href="https://msdn.microsoft.com/f969f249-6c1e-4c0c-8da6-ec7069b06e20">WSD_RESOLVE</a>



<a href="https://msdn.microsoft.com/eabcc3af-282c-4299-8061-6cddf14eca6b">WSD_RESOLVE_MATCH</a>
 

 

