---
UID: NF:wmcontainer.IMFASFStreamSelector.GetOutputFromStream
title: IMFASFStreamSelector::GetOutputFromStream
author: windows-sdk-content
description: Retrieves the output number associated with a stream.
old-location: mf\imfasfstreamselector_getoutputfromstream.htm
tech.root: medfound
ms.assetid: a7ff421b-3ef3-406a-ae05-8d8bf9f4357f
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetOutputFromStream, GetOutputFromStream method [Media Foundation], GetOutputFromStream method [Media Foundation],IMFASFStreamSelector interface, IMFASFStreamSelector interface [Media Foundation],GetOutputFromStream method, IMFASFStreamSelector.GetOutputFromStream, IMFASFStreamSelector::GetOutputFromStream, a7ff421b-3ef3-406a-ae05-8d8bf9f4357f, mf.imfasfstreamselector_getoutputfromstream, wmcontainer/IMFASFStreamSelector::GetOutputFromStream
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
 - IMFASFStreamSelector.GetOutputFromStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFStreamSelector::GetOutputFromStream


## -description



Retrieves the output number associated with a stream.




## -parameters




### -param wStreamNum [in]

The stream number for which to retrieve an output number.


### -param pdwOutput [out]

Receives the output number.


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
Invalid stream number.

</td>
</tr>
</table>
 




## -remarks



Outputs are streams in the ASF data section that will be parsed.




## -see-also




<a href="https://msdn.microsoft.com/d2e1fc15-2e12-4698-a4b1-ca8046d228de">IMFASFStreamSelector</a>
 

 

