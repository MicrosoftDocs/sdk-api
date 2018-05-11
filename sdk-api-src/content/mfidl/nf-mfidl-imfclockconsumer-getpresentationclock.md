---
UID: NF:mfidl.IMFClockConsumer.GetPresentationClock
title: IMFClockConsumer::GetPresentationClock
author: windows-driver-content
description: Called by the media pipeline to get an instance of IMFPresentationClock.
old-location: mf\imfclockconsumer_getpresentationclock.htm
old-project: medfound
ms.assetid: 92EC184F-EF13-4453-B1C0-D7DCD4C7F44C
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetPresentationClock, GetPresentationClock method [Media Foundation], GetPresentationClock method [Media Foundation],IMFClockConsumer interface, IMFClockConsumer interface [Media Foundation],GetPresentationClock method, IMFClockConsumer.GetPresentationClock, IMFClockConsumer::GetPresentationClock, mf.imfclockconsumer_getpresentationclock, mfidl/IMFClockConsumer::GetPresentationClock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
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
-	mfplat.lib
-	mfplat.dll
-	mfplat.dll
-	mfplat.dll.dll
api_name:
-	IMFClockConsumer.GetPresentationClock
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFClockConsumer::GetPresentationClock


## -description


Called by the media pipeline to get an instance of <a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a>. 


## -parameters




### -param ppPresentationClock [out]

Pointer to an object that implements the <a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a> interface. This value can be null.


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

                The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">

                The app does not implement this method.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/B21D3797-695F-4794-80A2-05D381F288C2">IMFClockConsumer</a>
 

 

