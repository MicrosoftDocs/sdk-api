---
UID: NF:mfidl.IMFClockConsumer.SetPresentationClock
title: IMFClockConsumer::SetPresentationClock (mfidl.h)
author: windows-sdk-content
description: Called by the media pipeline to provide the app with an instance of IMFPresentationClock.
old-location: mf\imfclockconsumer_setpresentationclock.htm
tech.root: medfound
ms.assetid: 7F4CC427-1DBE-4586-BA67-7AB472A55408
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFClockConsumer interface [Media Foundation],SetPresentationClock method, IMFClockConsumer.SetPresentationClock, IMFClockConsumer::SetPresentationClock, SetPresentationClock, SetPresentationClock method [Media Foundation], SetPresentationClock method [Media Foundation],IMFClockConsumer interface, mf.imfclockconsumer_setpresentationclock, mfidl/IMFClockConsumer::SetPresentationClock
ms.topic: method
f1_keywords: 
 - "mfidl/IMFClockConsumer.SetPresentationClock"
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFClockConsumer.SetPresentationClock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFClockConsumer::SetPresentationClock


## -description


Called by the media pipeline to provide the app with an instance of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>.


## -parameters




### -param pPresentationClock [in]

An instance of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>.


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
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfclockconsumer">IMFClockConsumer</a>
 

 

