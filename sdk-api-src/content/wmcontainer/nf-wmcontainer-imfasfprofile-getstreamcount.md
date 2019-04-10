---
UID: NF:wmcontainer.IMFASFProfile.GetStreamCount
title: IMFASFProfile::GetStreamCount (wmcontainer.h)
author: windows-sdk-content
description: Retrieves the number of streams in the profile.
old-location: mf\imfasfprofile_getstreamcount.htm
tech.root: medfound
ms.assetid: bf8c6157-3420-4097-8ab6-f307a69d418a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStreamCount, GetStreamCount method [Media Foundation], GetStreamCount method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],GetStreamCount method, IMFASFProfile.GetStreamCount, IMFASFProfile::GetStreamCount, bf8c6157-3420-4097-8ab6-f307a69d418a, mf.imfasfprofile_getstreamcount, wmcontainer/IMFASFProfile::GetStreamCount
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
 - IMFASFProfile.GetStreamCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFProfile::GetStreamCount


## -description



Retrieves the number of streams in the profile.




## -parameters




### -param pcStreams [out]

Receives the number of streams in the profile.


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




<a href="https://msdn.microsoft.com/03a0981b-29c3-450d-aa58-bc56a76e6cb6">ASF Profile</a>



<a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a>



<a href="https://msdn.microsoft.com/918f6534-811e-42f6-9836-1c77816007fa">IMFASFProfile::GetStream</a>



<a href="https://msdn.microsoft.com/c2272260-74ab-42ff-bff3-d6c6d5b322f3">IMFASFProfile::SetStream</a>
 

 

