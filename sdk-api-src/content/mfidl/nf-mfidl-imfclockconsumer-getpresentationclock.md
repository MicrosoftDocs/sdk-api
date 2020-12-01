---
UID: NF:mfidl.IMFClockConsumer.GetPresentationClock
title: IMFClockConsumer::GetPresentationClock (mfidl.h)
description: Called by the media pipeline to get an instance of IMFPresentationClock.
helpviewer_keywords: ["GetPresentationClock","GetPresentationClock method [Media Foundation]","GetPresentationClock method [Media Foundation]","IMFClockConsumer interface","IMFClockConsumer interface [Media Foundation]","GetPresentationClock method","IMFClockConsumer.GetPresentationClock","IMFClockConsumer::GetPresentationClock","mf.imfclockconsumer_getpresentationclock","mfidl/IMFClockConsumer::GetPresentationClock"]
old-location: mf\imfclockconsumer_getpresentationclock.htm
tech.root: mf
ms.assetid: 92EC184F-EF13-4453-B1C0-D7DCD4C7F44C
ms.date: 12/05/2018
ms.keywords: GetPresentationClock, GetPresentationClock method [Media Foundation], GetPresentationClock method [Media Foundation],IMFClockConsumer interface, IMFClockConsumer interface [Media Foundation],GetPresentationClock method, IMFClockConsumer.GetPresentationClock, IMFClockConsumer::GetPresentationClock, mf.imfclockconsumer_getpresentationclock, mfidl/IMFClockConsumer::GetPresentationClock
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFClockConsumer::GetPresentationClock
 - mfidl/IMFClockConsumer::GetPresentationClock
dev_langs:
 - c++
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
 - IMFClockConsumer.GetPresentationClock
---

# IMFClockConsumer::GetPresentationClock


## -description

Called by the media pipeline to get an instance of <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>.

## -parameters

### -param ppPresentationClock [out]

Pointer to an object that implements the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a> interface. This value can be null.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockconsumer">IMFClockConsumer</a>