---
UID: NF:wmcontainer.IMFASFStreamSelector.GetOutputStreamCount
title: IMFASFStreamSelector::GetOutputStreamCount (wmcontainer.h)
author: windows-sdk-content
description: Retrieves the number of streams associated with an output.
old-location: mf\imfasfstreamselector_getoutputstreamcount.htm
tech.root: medfound
ms.assetid: 928e958b-55dc-4939-8ac3-282389f0077a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 928e958b-55dc-4939-8ac3-282389f0077a, GetOutputStreamCount, GetOutputStreamCount method [Media Foundation], GetOutputStreamCount method [Media Foundation],IMFASFStreamSelector interface, IMFASFStreamSelector interface [Media Foundation],GetOutputStreamCount method, IMFASFStreamSelector.GetOutputStreamCount, IMFASFStreamSelector::GetOutputStreamCount, mf.imfasfstreamselector_getoutputstreamcount, wmcontainer/IMFASFStreamSelector::GetOutputStreamCount
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
 - IMFASFStreamSelector.GetOutputStreamCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFStreamSelector::GetOutputStreamCount


## -description



Retrieves the number of streams associated with an output.




## -parameters




### -param dwOutputNum [in]

The output number for which to retrieve the stream count.


### -param pcStreams [out]

Receives the number of streams associated with the output.


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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Invalid output number.

</td>
</tr>
</table>
 




## -remarks



An output is a stream in an ASF data section that will be parsed. If mutual exclusion is used, mutually exclusive streams share the same output.




## -see-also




<a href="https://msdn.microsoft.com/d2e1fc15-2e12-4698-a4b1-ca8046d228de">IMFASFStreamSelector</a>
 

 

