---
UID: NF:wtsprotocol.IWRdsProtocolShadowCallback.StopShadow
title: IWRdsProtocolShadowCallback::StopShadow (wtsprotocol.h)
author: windows-sdk-content
description: Instructs the Remote Desktop Services service to stop shadowing a target.
old-location: termserv\iwrdsprotocolshadowcallback_stopshadow.htm
tech.root: TermServ
ms.assetid: 09911813-554d-4ce1-b34e-5a6f57ec286d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolShadowCallback interface [Remote Desktop Services],StopShadow method, IWRdsProtocolShadowCallback.StopShadow, IWRdsProtocolShadowCallback::StopShadow, StopShadow, StopShadow method [Remote Desktop Services], StopShadow method [Remote Desktop Services],IWRdsProtocolShadowCallback interface, termserv.iwrdsprotocolshadowcallback_stopshadow, wtsprotocol/IWRdsProtocolShadowCallback::StopShadow
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
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
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolShadowCallback.StopShadow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolShadowCallback::StopShadow


## -description


Instructs the Remote Desktop Services service to stop shadowing a target. This method is called in response to a call of <a href="https://msdn.microsoft.com/9fe2e3fb-f368-4b7e-b679-402db900916c">DoTarget</a> by the shadow client.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/47727d33-df3d-49da-bc82-a4ed5ce0a381">IWRdsProtocolShadowCallback</a>
 

 

