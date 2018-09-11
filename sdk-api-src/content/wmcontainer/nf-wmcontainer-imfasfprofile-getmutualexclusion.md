---
UID: NF:wmcontainer.IMFASFProfile.GetMutualExclusion
title: IMFASFProfile::GetMutualExclusion
author: windows-sdk-content
description: Retrieves an Advanced Systems Format (ASF) mutual exclusion object from the profile.
old-location: mf\imfasfprofile_getmutualexclusion.htm
tech.root: medfound
ms.assetid: 9b9e37fc-0bd8-4502-9e90-76330a08f68b
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 9b9e37fc-0bd8-4502-9e90-76330a08f68b, GetMutualExclusion, GetMutualExclusion method [Media Foundation], GetMutualExclusion method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],GetMutualExclusion method, IMFASFProfile.GetMutualExclusion, IMFASFProfile::GetMutualExclusion, mf.imfasfprofile_getmutualexclusion, wmcontainer/IMFASFProfile::GetMutualExclusion
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
 - IMFASFProfile.GetMutualExclusion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFProfile::GetMutualExclusion


## -description



Retrieves an Advanced Systems Format (ASF) mutual exclusion object from the profile.




## -parameters




### -param dwMutexIndex [in]

Index of the mutual exclusion object in the profile.


### -param ppIMutex [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a> interface of the ASF mutual exclusion object. The caller must release the interface.


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



This method does not create a copy of the mutual exclusion object. The returned pointer refers to the mutual exclusion contained in the profile object. You must not make any changes to the mutual exclusion object using this pointer, because doing so can affect the profile object in unexpected ways.

To change the configuration of the mutual exclusion object in the profile, you must first clone the mutual exclusion object by calling <a href="https://msdn.microsoft.com/32bd09d7-9d85-4692-8b2f-6afab3234fa9">IMFASFMutualExclusion::Clone</a>. Make whatever changes are required to the clone of the object, remove the old mutual exclusion object from the profile by calling the <a href="https://msdn.microsoft.com/dbcf192f-1ab4-44c4-8444-5d2aba941fe1">IMFASFProfile::RemoveMutualExclusion</a> method, and then add the updated object by calling the <a href="https://msdn.microsoft.com/d9069feb-7d39-4b40-b95e-0112d959bbae">IMFASFProfile::AddMutualExclusion</a> method.




## -see-also




<a href="https://msdn.microsoft.com/03a0981b-29c3-450d-aa58-bc56a76e6cb6">ASF Profile</a>



<a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a>



<a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a>



<a href="https://msdn.microsoft.com/d9069feb-7d39-4b40-b95e-0112d959bbae">IMFASFProfile::AddMutualExclusion</a>



<a href="https://msdn.microsoft.com/5e275b83-9e59-4730-b8e2-e45f78077891">IMFASFProfile::GetMutualExclusionCount</a>



<a href="https://msdn.microsoft.com/dbcf192f-1ab4-44c4-8444-5d2aba941fe1">IMFASFProfile::RemoveMutualExclusion</a>
 

 

