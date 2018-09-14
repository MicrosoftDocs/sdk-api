---
UID: NF:wmcontainer.IMFASFProfile.RemoveStream
title: IMFASFProfile::RemoveStream
author: windows-sdk-content
description: Removes a stream from the Advanced Systems Format (ASF) profile object.
old-location: mf\imfasfprofile_removestream.htm
tech.root: medfound
ms.assetid: dfe404d3-66ea-407b-a2e0-caa065f41afe
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMFASFProfile interface [Media Foundation],RemoveStream method, IMFASFProfile.RemoveStream, IMFASFProfile::RemoveStream, RemoveStream, RemoveStream method [Media Foundation], RemoveStream method [Media Foundation],IMFASFProfile interface, dfe404d3-66ea-407b-a2e0-caa065f41afe, mf.imfasfprofile_removestream, wmcontainer/IMFASFProfile::RemoveStream
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
 - IMFASFProfile.RemoveStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFProfile::RemoveStream


## -description



Removes a stream from the Advanced Systems Format (ASF) profile object.




## -parameters




### -param wStreamNumber [in]

Stream number of the stream to remove.


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



After a stream is removed, the ASF profile object reassigns stream indexes so that the index values are sequential starting from zero. Any previously stored stream index numbers are no longer valid after deleting a stream.




## -see-also




<a href="https://msdn.microsoft.com/03a0981b-29c3-450d-aa58-bc56a76e6cb6">ASF Profile</a>



<a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a>



<a href="https://msdn.microsoft.com/918f6534-811e-42f6-9836-1c77816007fa">IMFASFProfile::GetStream</a>



<a href="https://msdn.microsoft.com/c2272260-74ab-42ff-bff3-d6c6d5b322f3">IMFASFProfile::SetStream</a>
 

 

