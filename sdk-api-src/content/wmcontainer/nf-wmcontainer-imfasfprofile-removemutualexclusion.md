---
UID: NF:wmcontainer.IMFASFProfile.RemoveMutualExclusion
title: IMFASFProfile::RemoveMutualExclusion
author: windows-sdk-content
description: Removes an Advanced Systems Format (ASF) mutual exclusion object from the profile.
old-location: mf\imfasfprofile_removemutualexclusion.htm
old-project: medfound
ms.assetid: dbcf192f-1ab4-44c4-8444-5d2aba941fe1
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMFASFProfile interface [Media Foundation],RemoveMutualExclusion method, IMFASFProfile.RemoveMutualExclusion, IMFASFProfile::RemoveMutualExclusion, RemoveMutualExclusion, RemoveMutualExclusion method [Media Foundation], RemoveMutualExclusion method [Media Foundation],IMFASFProfile interface, dbcf192f-1ab4-44c4-8444-5d2aba941fe1, mf.imfasfprofile_removemutualexclusion, wmcontainer/IMFASFProfile::RemoveMutualExclusion
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
 - IMFASFProfile.RemoveMutualExclusion
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFProfile::RemoveMutualExclusion


## -description



Removes an Advanced Systems Format (ASF) mutual exclusion object from the profile.




## -parameters




### -param dwMutexIndex [in]

The index of the mutual exclusion object to remove from the profile.


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



When a mutual exclusion object is removed from the profile, the ASF profile object reassigns the mutual exclusion indexes so that they are sequential starting with zero. Any previously stored indexes are no longer valid after calling this method.




## -see-also




<a href="https://msdn.microsoft.com/03a0981b-29c3-450d-aa58-bc56a76e6cb6">ASF Profile</a>



<a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a>



<a href="https://msdn.microsoft.com/d9069feb-7d39-4b40-b95e-0112d959bbae">IMFASFProfile::AddMutualExclusion</a>



<a href="https://msdn.microsoft.com/9b9e37fc-0bd8-4502-9e90-76330a08f68b">IMFASFProfile::GetMutualExclusion</a>
 

 

