---
UID: NF:wmcontainer.IMFASFMutualExclusion.RemoveRecord
title: IMFASFMutualExclusion::RemoveRecord
author: windows-sdk-content
description: Removes a record from the Advanced Systems Format (ASF) mutual exclusion object.
old-location: mf\imfasfmutualexclusion_removerecord.htm
old-project: medfound
ms.assetid: ecfb5e10-5102-4f6a-b67b-ba0ed06d0ed8
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFASFMutualExclusion interface [Media Foundation],RemoveRecord method, IMFASFMutualExclusion.RemoveRecord, IMFASFMutualExclusion::RemoveRecord, RemoveRecord, RemoveRecord method [Media Foundation], RemoveRecord method [Media Foundation],IMFASFMutualExclusion interface, ecfb5e10-5102-4f6a-b67b-ba0ed06d0ed8, mf.imfasfmutualexclusion_removerecord, wmcontainer/IMFASFMutualExclusion::RemoveRecord
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
 - IMFASFMutualExclusion.RemoveRecord
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFMutualExclusion::RemoveRecord


## -description



Removes a record from the Advanced Systems Format (ASF) mutual exclusion object.




## -parameters




### -param dwRecordNumber [in]

The index of the record to remove.


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



When a record is removed, the ASF mutual exclusion object indexes the remaining records so that they are sequential starting with zero. You should enumerate the records to ensure that you have the correct index for each record. If the record removed is the one with the highest index, removing it has no effect on the other indexes.




## -see-also




<a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a>



<a href="https://msdn.microsoft.com/f5dedc87-a29c-4c8d-b493-486d975f9ac4">IMFASFMutualExclusion::AddRecord</a>



<a href="https://msdn.microsoft.com/fdd31eac-1dd6-45f0-90fb-d5a74c85db2e">Using Mutual Exclusion for ASF Streams</a>
 

 

