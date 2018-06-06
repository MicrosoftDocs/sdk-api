---
UID: NF:wmcontainer.IMFASFMultiplexer.Flush
title: IMFASFMultiplexer::Flush
author: windows-sdk-content
description: Signals the multiplexer to process all queued output media samples. Call this method after passing the last sample to the multiplexer.
old-location: mf\imfasfmultiplexer_flush.htm
old-project: medfound
ms.assetid: 44a66374-ad9d-4c76-8c95-21a15e071c6d
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 44a66374-ad9d-4c76-8c95-21a15e071c6d, Flush, Flush method [Media Foundation], Flush method [Media Foundation],IMFASFMultiplexer interface, IMFASFMultiplexer interface [Media Foundation],Flush method, IMFASFMultiplexer.Flush, IMFASFMultiplexer::Flush, mf.imfasfmultiplexer_flush, wmcontainer/IMFASFMultiplexer::Flush
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFMultiplexer.Flush
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFMultiplexer::Flush


## -description



Signals the multiplexer to process all queued output media samples. Call this method after passing the last sample to the multiplexer.




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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



You must call <b>Flush</b> after the last sample has been passed into the ASF multiplexer and before you call <a href="https://msdn.microsoft.com/2a106ea5-976a-40df-a554-1b76d9a07286">IMFASFMultiplexer::End</a>. This causes all output media samples in progress to be completed. After calling <b>Flush</b>, call <a href="https://msdn.microsoft.com/39b9f8a0-fb26-4f46-98fd-b4636f8f88c7">IMFASFMultiplexer::GetNextPacket</a> in a loop until all the pending media samples have been packetized.




## -see-also




<a href="https://msdn.microsoft.com/7afa9694-c965-40e2-8549-e32ff48def2a">Generating New ASF Data Packets</a>



<a href="https://msdn.microsoft.com/bdb549b5-425b-4f77-b413-723ceb7acd11">IMFASFMultiplexer</a>
 

 

