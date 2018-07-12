---
UID: NF:wmcontainer.IMFASFStreamConfig.GetMediaType
title: IMFASFStreamConfig::GetMediaType
author: windows-sdk-content
description: Retrieves the media type of the stream.
old-location: mf\imfasfstreamconfig_getmediatype.htm
old-project: medfound
ms.assetid: 6311115a-26e6-47b7-b724-0209a5bf45d7
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 6311115a-26e6-47b7-b724-0209a5bf45d7, GetMediaType, GetMediaType method [Media Foundation], GetMediaType method [Media Foundation],IMFASFStreamConfig interface, IMFASFStreamConfig interface [Media Foundation],GetMediaType method, IMFASFStreamConfig.GetMediaType, IMFASFStreamConfig::GetMediaType, mf.imfasfstreamconfig_getmediatype, wmcontainer/IMFASFStreamConfig::GetMediaType
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
 - IMFASFStreamConfig.GetMediaType
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFStreamConfig::GetMediaType


## -description



Retrieves the media type of the stream.




## -parameters




### -param ppIMediaType [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type object associated with the stream. The caller must release the interface.


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



To reduce unnecessary copying, the method returns a pointer to the media type  that is stored internally by the object. Do not modify the returned media type,  as the results are not defined.




## -see-also




<a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a>



<a href="https://msdn.microsoft.com/53b7c4fd-a3bc-4e15-b2f6-380cae8ab2f6">IMFASFStreamConfig::SetMediaType</a>



<a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a>
 

 

