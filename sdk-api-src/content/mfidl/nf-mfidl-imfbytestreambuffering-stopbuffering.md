---
UID: NF:mfidl.IMFByteStreamBuffering.StopBuffering
title: IMFByteStreamBuffering::StopBuffering
author: windows-driver-content
description: Stops any buffering that is in progress.
old-location: mf\imfbytestreambuffering_stopbuffering.htm
old-project: medfound
ms.assetid: da342ac4-bb61-40d6-9b67-0480ac2a780f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMFByteStreamBuffering interface [Media Foundation],StopBuffering method, IMFByteStreamBuffering.StopBuffering, IMFByteStreamBuffering::StopBuffering, StopBuffering, StopBuffering method [Media Foundation], StopBuffering method [Media Foundation],IMFByteStreamBuffering interface, da342ac4-bb61-40d6-9b67-0480ac2a780f, mf.imfbytestreambuffering_stopbuffering, mfidl/IMFByteStreamBuffering::StopBuffering
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFByteStreamBuffering.StopBuffering
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFByteStreamBuffering::StopBuffering


## -description



Stops any buffering that is in progress.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The byte stream successfully stopped buffering.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No buffering was in progress.

</td>
</tr>
</table>
 




## -remarks



If the byte stream is currently buffering data, it stops and sends an <a href="https://msdn.microsoft.com/11b1290d-d462-4aa0-a358-b3f6447c99d8">MEBufferingStopped</a> event. If the byte stream is not currently buffering, this method has no effect.




## -see-also




<a href="https://msdn.microsoft.com/bbf9cdb1-5ec7-498a-aa59-85c24779547e">IMFByteStreamBuffering</a>
 

 

