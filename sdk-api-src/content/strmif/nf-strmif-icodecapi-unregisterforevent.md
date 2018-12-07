---
UID: NF:strmif.ICodecAPI.UnregisterForEvent
title: ICodecAPI::UnregisterForEvent
author: windows-sdk-content
description: The UnregisterForEvent method unregisters the application for a specified encoder event.
old-location: dshow\icodecapi_unregisterforevent.htm
tech.root: DirectShow
ms.assetid: d6f48379-664a-498f-8872-2272778588db
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICodecAPI interface [DirectShow],UnregisterForEvent method, ICodecAPI.UnregisterForEvent, ICodecAPI::UnregisterForEvent, ICodecAPIUnregisterForEvent, UnregisterForEvent, UnregisterForEvent method [DirectShow], UnregisterForEvent method [DirectShow],ICodecAPI interface, dshow.icodecapi_unregisterforevent, strmif/ICodecAPI::UnregisterForEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICodecAPI.UnregisterForEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICodecAPI::UnregisterForEvent


## -description



The <b>UnregisterForEvent</b> method unregisters the application for a specified encoder event.




## -parameters




### -param Api [in]

Pointer to a GUID that specifies the event.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/82085fd5-2d31-48a0-b2ef-0eede4de60c8">Codec API Reference</a>



<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>



<a href="https://msdn.microsoft.com/87423ddb-7011-40ab-a449-eb43688efb26">ICodecAPI::RegisterForEvent</a>
 

 

