---
UID: NF:wmcontainer.IMFASFProfile.GetMutualExclusionCount
title: IMFASFProfile::GetMutualExclusionCount (wmcontainer.h)
author: windows-sdk-content
description: Retrieves the number of Advanced Systems Format (ASF) mutual exclusion objects that are associated with the profile.
old-location: mf\imfasfprofile_getmutualexclusioncount.htm
tech.root: medfound
ms.assetid: 5e275b83-9e59-4730-b8e2-e45f78077891
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5e275b83-9e59-4730-b8e2-e45f78077891, GetMutualExclusionCount, GetMutualExclusionCount method [Media Foundation], GetMutualExclusionCount method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],GetMutualExclusionCount method, IMFASFProfile.GetMutualExclusionCount, IMFASFProfile::GetMutualExclusionCount, mf.imfasfprofile_getmutualexclusioncount, wmcontainer/IMFASFProfile::GetMutualExclusionCount
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
 - IMFASFProfile.GetMutualExclusionCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFProfile::GetMutualExclusionCount


## -description



Retrieves the number of Advanced Systems Format (ASF) mutual exclusion objects that are associated with the profile.




## -parameters




### -param pcMutexs [out]

Receives the number of mutual exclusion objects.


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



Multiple mutual exclusion objects may be required for streams that are mutually exclusive in more than one way. For more information, see <a href="https://msdn.microsoft.com/f5dedc87-a29c-4c8d-b493-486d975f9ac4">IMFASFMutualExclusion::AddRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/03a0981b-29c3-450d-aa58-bc56a76e6cb6">ASF Profile</a>



<a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a>



<a href="https://msdn.microsoft.com/9b9e37fc-0bd8-4502-9e90-76330a08f68b">IMFASFProfile::GetMutualExclusion</a>
 

 

