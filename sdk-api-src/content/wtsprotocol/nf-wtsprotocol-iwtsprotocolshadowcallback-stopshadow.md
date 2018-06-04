---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWTSProtocolShadowCallback::StopShadow


## -description


<p class="CCE_Message">[<b>IWTSProtocolShadowCallback::StopShadow</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/09911813-554d-4ce1-b34e-5a6f57ec286d">IWRdsProtocolShadowCallback::StopShadow</a>.]

Instructs the Remote Desktop Services service to stop shadowing a target. This method is called in response to a call of <a href="https://msdn.microsoft.com/437983a4-48a4-4b37-99ba-35fe1f03b3ec">DoTarget</a> by the shadow client.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/ce224b9f-161c-4133-97d9-05c339eefb77">IWTSProtocolShadowCallback</a>
 

 

