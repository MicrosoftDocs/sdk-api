---
UID: NF:strmif.IAMExtTransport.get_Mode
title: IAMExtTransport::get_Mode (strmif.h)
author: windows-sdk-content
description: The get_Mode method retrieves the current transport mode, such as play, stop, or record.
old-location: dshow\iamexttransport_get_mode.htm
tech.root: DirectShow
ms.assetid: ee08cca0-a2ea-4a7c-8714-f22d5cd62fe8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMExtTransport interface [DirectShow],get_Mode method, IAMExtTransport.get_Mode, IAMExtTransport::get_Mode, IAMExtTransportget_Mode, dshow.iamexttransport_get_mode, get_Mode, get_Mode method [DirectShow], get_Mode method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::get_Mode
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
 - IAMExtTransport.get_Mode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMExtTransport::get_Mode


## -description



The <code>get_Mode</code> method retrieves the current transport mode, such as play, stop, or record.




## -parameters




### -param pMode [out]

Pointer to a <b>long</b> integer that receives the current transport mode. For possible values, see <a href="https://msdn.microsoft.com/cf941c07-6f42-4c63-9bdf-923f7a5b0b02">IAMExtTransport::put_Mode</a>.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>
 

 

