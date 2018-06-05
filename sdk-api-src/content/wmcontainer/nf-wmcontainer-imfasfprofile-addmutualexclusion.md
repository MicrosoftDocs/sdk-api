---
UID: NF:wmcontainer.IMFASFProfile.AddMutualExclusion
title: IMFASFProfile::AddMutualExclusion
author: windows-sdk-content
description: Adds a configured Advanced Systems Format (ASF) mutual exclusion object to the profile.
old-location: mf\imfasfprofile_addmutualexclusion.htm
old-project: medfound
ms.assetid: d9069feb-7d39-4b40-b95e-0112d959bbae
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AddMutualExclusion, AddMutualExclusion method [Media Foundation], AddMutualExclusion method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],AddMutualExclusion method, IMFASFProfile.AddMutualExclusion, IMFASFProfile::AddMutualExclusion, d9069feb-7d39-4b40-b95e-0112d959bbae, mf.imfasfprofile_addmutualexclusion, wmcontainer/IMFASFProfile::AddMutualExclusion
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFASFProfile.AddMutualExclusion
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFProfile::AddMutualExclusion


## -description



Adds a configured Advanced Systems Format (ASF) mutual exclusion object to the profile.




## -parameters




### -param pIMutex [in]

Pointer to the <a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a> interface of a configured ASF mutual exclusion object.


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



You can create a mutual exclusion object by calling the <a href="https://msdn.microsoft.com/457b7b73-34c0-48fe-882a-9cdc3516e20d">IMFASFProfile::CreateMutualExclusion</a> method.




## -see-also




<a href="https://msdn.microsoft.com/03a0981b-29c3-450d-aa58-bc56a76e6cb6">ASF Profile</a>



<a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a>



<a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a>



<a href="https://msdn.microsoft.com/9b9e37fc-0bd8-4502-9e90-76330a08f68b">IMFASFProfile::GetMutualExclusion</a>



<a href="https://msdn.microsoft.com/dbcf192f-1ab4-44c4-8444-5d2aba941fe1">IMFASFProfile::RemoveMutualExclusion</a>
 

 

