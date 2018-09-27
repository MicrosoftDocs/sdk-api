---
UID: NF:strmif.IAMExtTransport.get_Rate
title: IAMExtTransport::get_Rate
author: windows-sdk-content
description: The get_Rate method retrieves the playback rate for variable-speed external devices.
old-location: dshow\iamexttransport_get_rate.htm
tech.root: DirectShow
ms.assetid: 35a2fb2b-0963-4bdb-86a4-b5950b48a834
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAMExtTransport interface [DirectShow],get_Rate method, IAMExtTransport.get_Rate, IAMExtTransport::get_Rate, IAMExtTransportget_Rate, dshow.iamexttransport_get_rate, get_Rate, get_Rate method [DirectShow], get_Rate method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::get_Rate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMExtTransport.get_Rate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMExtTransport::get_Rate


## -description



The <code>get_Rate</code> method retrieves the playback rate for variable-speed external devices.



This method is not implemented.


## -parameters




### -param pdblRate [out]

Pointer to a <b>double</b> to receive the playback rate that was set using <a href="https://msdn.microsoft.com/165966f1-f826-4ce2-b520-4a420898eee4">IAMExtTransport::put_Rate</a>.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>
 

 

