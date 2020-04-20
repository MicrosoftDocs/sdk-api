---
UID: NF:wmcontainer.IMFASFMultiplexer.GetStatistics
title: IMFASFMultiplexer::GetStatistics (wmcontainer.h)
description: Retrieves multiplexer statistics.helpviewer_keywords: ["56083ceb-3d39-4fda-995a-f91fa0e16853","GetStatistics","GetStatistics method [Media Foundation]","GetStatistics method [Media Foundation]","IMFASFMultiplexer interface","IMFASFMultiplexer interface [Media Foundation]","GetStatistics method","IMFASFMultiplexer.GetStatistics","IMFASFMultiplexer::GetStatistics","mf.imfasfmultiplexer_getstatistics","wmcontainer/IMFASFMultiplexer::GetStatistics"]
old-location: mf\imfasfmultiplexer_getstatistics.htm
tech.root: medfound
ms.assetid: 56083ceb-3d39-4fda-995a-f91fa0e16853
ms.date: 12/05/2018
ms.keywords: 56083ceb-3d39-4fda-995a-f91fa0e16853, GetStatistics, GetStatistics method [Media Foundation], GetStatistics method [Media Foundation],IMFASFMultiplexer interface, IMFASFMultiplexer interface [Media Foundation],GetStatistics method, IMFASFMultiplexer.GetStatistics, IMFASFMultiplexer::GetStatistics, mf.imfasfmultiplexer_getstatistics, wmcontainer/IMFASFMultiplexer::GetStatistics
f1_keywords:
- wmcontainer/IMFASFMultiplexer.GetStatistics
dev_langs:
- c++
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFASFMultiplexer.GetStatistics
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFASFMultiplexer::GetStatistics


## -description



Retrieves multiplexer statistics.




## -parameters




### -param wStreamNumber [in]

The stream number for which to obtain statistics.


### -param pMuxStats [out]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_mux_statistics">ASF_MUX_STATISTICS</a> structure that receives the statistics.


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




<a href="https://docs.microsoft.com/windows/desktop/medfound/generating-new-asf-data-packets">Generating New ASF Data Packets</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer">IMFASFMultiplexer</a>
 

 

