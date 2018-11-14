---
UID: NN:rdpencomapi.IRDPSRAPIApplicationFilter
title: IRDPSRAPIApplicationFilter
author: windows-sdk-content
description: Manages the shared desktop area at the window and process level. Applications can use the enumerators to display lists of objects in the session that can be shared.
old-location: rdp\irdpsrapiapplicationfilter.htm
tech.root: Rdp
ms.assetid: 6a08c948-1b25-4a36-93c8-23e7e3f4fb08
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IRDPSRAPIApplicationFilter, IRDPSRAPIApplicationFilter interface [RDP], IRDPSRAPIApplicationFilter interface [RDP],described, rdp.irdpsrapiapplicationfilter, rdpencomapi/IRDPSRAPIApplicationFilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IRDPSRAPIApplicationFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPSRAPIApplicationFilter interface


## -description


Manages the shared desktop area at the window and process level. Applications can use the enumerators to display lists of objects in the session that can be shared.

Applications can obtain access to this object using <a href="https://msdn.microsoft.com/4a346305-972c-40c4-882e-905745edf6e9">IRDPSRAPISharingSession::ApplicationFilter</a>.

The list of sharable objects is exposed as a two-level tree. Each window has an application object as a parent. Each window object has its own sharing state that can be overridden by the sharing state of its parent. Each application object has its own sharing state that can be overridden by the <a href="https://msdn.microsoft.com/91d8fdea-3fe0-4623-ab83-ce3927321bbc">Enabled</a> property of the application filter. Therefore, if an application filter is enabled and the application is shared, its windows are shared regardless of their sharing state. If the application filter is enabled but the application is not shared, its windows are shared depending on their sharing state.

If a shared application creates a new window that is sharable, it will be shared because the parent application is shared.


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/9a934718-1eea-4406-a1da-b7d493f6667e">IRDPSRAPIApplication</a>



<a href="https://msdn.microsoft.com/275bb93c-dc93-4884-82a9-e87f5c3ab475">IRDPSRAPIApplicationList</a>
 

 

