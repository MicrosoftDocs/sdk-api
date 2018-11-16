---
UID: NF:wmcontainer.IMFASFProfile.CreateMutualExclusion
title: IMFASFProfile::CreateMutualExclusion
author: windows-sdk-content
description: Creates a new Advanced Systems Format (ASF) mutual exclusion object. Mutual exclusion objects can be added to a profile by calling the AddMutualExclusion method.
old-location: mf\imfasfprofile_createmutualexclusion.htm
tech.root: medfound
ms.assetid: 457b7b73-34c0-48fe-882a-9cdc3516e20d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 457b7b73-34c0-48fe-882a-9cdc3516e20d, CreateMutualExclusion, CreateMutualExclusion method [Media Foundation], CreateMutualExclusion method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],CreateMutualExclusion method, IMFASFProfile.CreateMutualExclusion, IMFASFProfile::CreateMutualExclusion, mf.imfasfprofile_createmutualexclusion, wmcontainer/IMFASFProfile::CreateMutualExclusion
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
 - IMFASFProfile.CreateMutualExclusion
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
- IMFASFProfile.CreateMutualExclusion
: 
---

# IMFASFProfile::CreateMutualExclusion


## -description



Creates a new Advanced Systems Format (ASF) mutual exclusion object. Mutual exclusion objects can be added to a profile by calling the <a href="https://msdn.microsoft.com/d9069feb-7d39-4b40-b95e-0112d959bbae">AddMutualExclusion</a> method.




## -parameters




### -param ppIMutex [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a> interface of the new object. The caller must release the interface.


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



The ASF mutual exclusion object created by this method is not associated with the profile. Call <a href="https://msdn.microsoft.com/d9069feb-7d39-4b40-b95e-0112d959bbae">IMFASFProfile::AddMutualExclusion</a> after configuring the object to make this association.




## -see-also




<a href="https://msdn.microsoft.com/03a0981b-29c3-450d-aa58-bc56a76e6cb6">ASF Profile</a>



<a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a>



<a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a>
 

 

