---
UID: NF:wmcontainer.IMFASFProfile.CreateStream
title: IMFASFProfile::CreateStream
author: windows-sdk-content
description: Creates an Advanced Systems Format (ASF) stream configuration object.
old-location: mf\imfasfprofile_createstream.htm
tech.root: MedFound
ms.assetid: 3da52c1a-24c0-456b-a9e8-57b5467eda2a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: 3da52c1a-24c0-456b-a9e8-57b5467eda2a, CreateStream, CreateStream method [Media Foundation], CreateStream method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],CreateStream method, IMFASFProfile.CreateStream, IMFASFProfile::CreateStream, mf.imfasfprofile_createstream, wmcontainer/IMFASFProfile::CreateStream
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
 - IMFASFProfile.CreateStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFProfile::CreateStream


## -description



Creates an Advanced Systems Format (ASF) stream configuration object.




## -parameters




### -param pIMediaType [in]

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of a configured media type.


### -param ppIStream [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a> interface of the new ASF stream configuration object. The caller must release the interface.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppIStream</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
stream configuration object could not be created due to insufficient memory.

</td>
</tr>
</table>
 




## -remarks



The ASF stream configuration object created by this method is not included in the profile. To include the stream, you must first configure the stream configuration and then call <a href="https://msdn.microsoft.com/c2272260-74ab-42ff-bff3-d6c6d5b322f3">IMFASFProfile::SetStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/03a0981b-29c3-450d-aa58-bc56a76e6cb6">ASF Profile</a>



<a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a>



<a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a>



<a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a>
 

 

