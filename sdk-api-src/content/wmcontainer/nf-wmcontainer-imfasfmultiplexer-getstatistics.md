---
UID: NF:wmcontainer.IMFASFMultiplexer.GetStatistics
title: IMFASFMultiplexer::GetStatistics
author: windows-driver-content
description: Retrieves multiplexer statistics.
old-location: mf\imfasfmultiplexer_getstatistics.htm
old-project: medfound
ms.assetid: 56083ceb-3d39-4fda-995a-f91fa0e16853
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: 56083ceb-3d39-4fda-995a-f91fa0e16853, GetStatistics, GetStatistics method [Media Foundation], GetStatistics method [Media Foundation],IMFASFMultiplexer interface, IMFASFMultiplexer interface [Media Foundation],GetStatistics method, IMFASFMultiplexer.GetStatistics, IMFASFMultiplexer::GetStatistics, mf.imfasfmultiplexer_getstatistics, wmcontainer/IMFASFMultiplexer::GetStatistics
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFASFMultiplexer.GetStatistics
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFMultiplexer::GetStatistics


## -description



Retrieves multiplexer statistics.




## -parameters




### -param wStreamNumber [in]

The stream number for which to obtain statistics.


### -param pMuxStats [out]

Pointer to an <a href="https://msdn.microsoft.com/353ee03d-b706-4a70-9eaf-c14b47b5159a">ASF_MUX_STATISTICS</a> structure that receives the statistics.


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




<a href="https://msdn.microsoft.com/7afa9694-c965-40e2-8549-e32ff48def2a">Generating New ASF Data Packets</a>



<a href="https://msdn.microsoft.com/bdb549b5-425b-4f77-b413-723ceb7acd11">IMFASFMultiplexer</a>
 

 

