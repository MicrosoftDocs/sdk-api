---
UID: NF:dshowasf.IConfigAsfWriter2.StreamNumFromPin
title: IConfigAsfWriter2::StreamNumFromPin
author: windows-sdk-content
description: The StreamNumFromPin method retrieves the stream number associated with the specified input pin.
old-location: dshow\iconfigasfwriter2_streamnumfrompin.htm
tech.root: DirectShow
ms.assetid: 374331ec-6665-4ed9-b4ee-6d33b1e2ef2c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IConfigAsfWriter2 interface [DirectShow],StreamNumFromPin method, IConfigAsfWriter2.StreamNumFromPin, IConfigAsfWriter2::StreamNumFromPin, IConfigAsfWriter2StreamNumFromPin, StreamNumFromPin, StreamNumFromPin method [DirectShow], StreamNumFromPin method [DirectShow],IConfigAsfWriter2 interface, dshow.iconfigasfwriter2_streamnumfrompin, dshowasf/IConfigAsfWriter2::StreamNumFromPin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IConfigAsfWriter2.StreamNumFromPin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConfigAsfWriter2::StreamNumFromPin


## -description



The <code>StreamNumFromPin</code> method retrieves the stream number associated with the specified input pin.




## -parameters




### -param pPin [in]

Pointer to the <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface on the input pin.


### -param pwStreamNum [out]

Receives the stream number.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



You may need to use the Windows Media Format SDK interfaces directly to manipulate a stream before running the filter graph. This method is provided because you cannot assume that an ASF stream number is the same as the DirectShow pin number.




## -see-also




<a href="https://msdn.microsoft.com/dffda43a-5831-4889-864f-81351b9e2bb3">Creating ASF Files in DirectShow</a>



<a href="https://msdn.microsoft.com/fd931a95-3678-46de-8f17-9e7c27087398">IConfigAsfWriter2 Interface</a>
 

 

