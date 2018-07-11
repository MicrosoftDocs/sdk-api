---
UID: NF:mfidl.IMFClockConsumer.SetPresentationClock
title: IMFClockConsumer::SetPresentationClock
author: windows-sdk-content
description: Called by the media pipeline to provide the app with an instance of IMFPresentationClock.
old-location: mf\imfclockconsumer_setpresentationclock.htm
old-project: medfound
ms.assetid: 7F4CC427-1DBE-4586-BA67-7AB472A55408
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMFClockConsumer interface [Media Foundation],SetPresentationClock method, IMFClockConsumer.SetPresentationClock, IMFClockConsumer::SetPresentationClock, SetPresentationClock, SetPresentationClock method [Media Foundation], SetPresentationClock method [Media Foundation],IMFClockConsumer interface, mf.imfclockconsumer_setpresentationclock, mfidl/IMFClockConsumer::SetPresentationClock
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFClockConsumer::SetPresentationClock


## -description


Called by the media pipeline to provide the app with an instance of <a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a>.


## -parameters




### -param pPresentationClock [in]

An instance of <a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a>.


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




<a href="https://msdn.microsoft.com/B21D3797-695F-4794-80A2-05D381F288C2">IMFClockConsumer</a>
 

 

