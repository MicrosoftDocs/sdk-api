---
UID: NF:wmcontainer.IMFASFStreamConfig.SetMediaType
title: IMFASFStreamConfig::SetMediaType
author: windows-sdk-content
description: Sets the media type for the Advanced Systems Format (ASF) stream configuration object.
old-location: mf\imfasfstreamconfig_setmediatype.htm
tech.root: medfound
ms.assetid: 53b7c4fd-a3bc-4e15-b2f6-380cae8ab2f6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 53b7c4fd-a3bc-4e15-b2f6-380cae8ab2f6, IMFASFStreamConfig interface [Media Foundation],SetMediaType method, IMFASFStreamConfig.SetMediaType, IMFASFStreamConfig::SetMediaType, SetMediaType, SetMediaType method [Media Foundation], SetMediaType method [Media Foundation],IMFASFStreamConfig interface, mf.imfasfstreamconfig_setmediatype, wmcontainer/IMFASFStreamConfig::SetMediaType
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
 - IMFASFStreamConfig.SetMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmcontainer.h
: 
- IMFASFStreamConfig.SetMediaType
: 
---

# IMFASFStreamConfig::SetMediaType


## -description



Sets the media type for the Advanced Systems Format (ASF) stream configuration object.




## -parameters




### -param pIMediaType [in]

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of a configured media type object.


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



Some validation of the media type is performed by this method. However, a media type can be successfully set, but cause an error when the stream is added to the profile.




## -see-also




<a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a>



<a href="https://msdn.microsoft.com/6311115a-26e6-47b7-b724-0209a5bf45d7">IMFASFStreamConfig::GetMediaType</a>



<a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a>
 

 

