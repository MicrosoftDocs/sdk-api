---
UID: NF:strmif.IAMExtTransport.put_Rate
title: IAMExtTransport::put_Rate
author: windows-sdk-content
description: The put_Rate method sets the playback rate for variable-speed external devices.
old-location: dshow\iamexttransport_put_rate.htm
tech.root: DirectShow
ms.assetid: 165966f1-f826-4ce2-b520-4a420898eee4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAMExtTransport interface [DirectShow],put_Rate method, IAMExtTransport.put_Rate, IAMExtTransport::put_Rate, IAMExtTransportput_Rate, dshow.iamexttransport_put_rate, put_Rate, put_Rate method [DirectShow], put_Rate method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::put_Rate
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
 - IAMExtTransport.put_Rate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMExtTransport::put_Rate


## -description



The <code>put_Rate</code> method sets the playback rate for variable-speed external devices.



This method is not implemented.


## -parameters




### -param dblRate [in]

Specifies the rate as a multiple of normal playback rate. For example, 0.5 specifies half speed, and 2.0 specifies double speed.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/35a2fb2b-0963-4bdb-86a4-b5950b48a834">IAMExtTransport::get_Rate</a>
 

 

