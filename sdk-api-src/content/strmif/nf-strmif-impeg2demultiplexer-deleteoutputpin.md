---
UID: NF:strmif.IMpeg2Demultiplexer.DeleteOutputPin
title: IMpeg2Demultiplexer::DeleteOutputPin
author: windows-sdk-content
description: The DeleteOutputPin method deletes the specified output pin.
old-location: dshow\impeg2demultiplexer_deleteoutputpin.htm
tech.root: DirectShow
ms.assetid: 6c6a0e38-54b8-4fa3-b37a-00073d40965d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DeleteOutputPin, DeleteOutputPin method [DirectShow], DeleteOutputPin method [DirectShow],IMpeg2Demultiplexer interface, IMpeg2Demultiplexer interface [DirectShow],DeleteOutputPin method, IMpeg2Demultiplexer.DeleteOutputPin, IMpeg2Demultiplexer::DeleteOutputPin, IMpeg2DemultiplexerDeleteOutputPin, dshow.impeg2demultiplexer_deleteoutputpin, strmif/IMpeg2Demultiplexer::DeleteOutputPin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IMpeg2Demultiplexer.DeleteOutputPin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMpeg2Demultiplexer::DeleteOutputPin


## -description



The <code>DeleteOutputPin</code> method deletes the specified output pin.




## -parameters




### -param pszPinName [in]

The friendly name of the pin as specified when the pin was created in a call to <b>CreateOutputPin</b>.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



Call this method only when you need to delete a pin while keeping the filter alive. When the filter is released, it will perform all necessary cleanup on the output pins.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e9242b96-0fc3-428e-b7ee-91a4f5e67305">IMpeg2Demultiplexer Interface</a>
 

 

