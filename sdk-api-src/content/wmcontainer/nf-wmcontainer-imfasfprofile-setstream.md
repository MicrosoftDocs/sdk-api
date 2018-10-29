---
UID: NF:wmcontainer.IMFASFProfile.SetStream
title: IMFASFProfile::SetStream
author: windows-sdk-content
description: Adds a stream to the profile or reconfigures an existing stream.
old-location: mf\imfasfprofile_setstream.htm
tech.root: medfound
ms.assetid: c2272260-74ab-42ff-bff3-d6c6d5b322f3
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFASFProfile interface [Media Foundation],SetStream method, IMFASFProfile.SetStream, IMFASFProfile::SetStream, SetStream, SetStream method [Media Foundation], SetStream method [Media Foundation],IMFASFProfile interface, c2272260-74ab-42ff-bff3-d6c6d5b322f3, mf.imfasfprofile_setstream, wmcontainer/IMFASFProfile::SetStream
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
 - IMFASFProfile.SetStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFProfile::SetStream


## -description



Adds a stream to the profile or reconfigures an existing stream.




## -parameters




### -param pIStream [in]

Pointer to the <a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a> interface of a configured ASF stream configuration object.


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



If the stream number in the ASF stream configuration object is already included in the profile, the information in the new object replaces the old one. If the profile does not contain a stream for the stream number, the ASF stream configuration object is added as a new stream.




## -see-also




<a href="https://msdn.microsoft.com/03a0981b-29c3-450d-aa58-bc56a76e6cb6">ASF Profile</a>



<a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a>



<a href="https://msdn.microsoft.com/918f6534-811e-42f6-9836-1c77816007fa">IMFASFProfile::GetStream</a>



<a href="https://msdn.microsoft.com/1e3fadf0-1549-4d51-b263-727b15c55023">IMFASFProfile::GetStreamByNumber</a>



<a href="https://msdn.microsoft.com/bf8c6157-3420-4097-8ab6-f307a69d418a">IMFASFProfile::GetStreamCount</a>



<a href="https://msdn.microsoft.com/dfe404d3-66ea-407b-a2e0-caa065f41afe">IMFASFProfile::RemoveStream</a>



<a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a>
 

 

