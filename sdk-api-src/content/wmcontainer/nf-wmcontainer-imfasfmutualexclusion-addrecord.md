---
UID: NF:wmcontainer.IMFASFMutualExclusion.AddRecord
title: IMFASFMutualExclusion::AddRecord
author: windows-sdk-content
description: Adds a record to the mutual exclusion object. A record specifies streams that are mutually exclusive with the streams in all other records.
old-location: mf\imfasfmutualexclusion_addrecord.htm
old-project: medfound
ms.assetid: f5dedc87-a29c-4c8d-b493-486d975f9ac4
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AddRecord, AddRecord method [Media Foundation], AddRecord method [Media Foundation],IMFASFMutualExclusion interface, IMFASFMutualExclusion interface [Media Foundation],AddRecord method, IMFASFMutualExclusion.AddRecord, IMFASFMutualExclusion::AddRecord, f5dedc87-a29c-4c8d-b493-486d975f9ac4, mf.imfasfmutualexclusion_addrecord, wmcontainer/IMFASFMutualExclusion::AddRecord
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
-	IMFASFMutualExclusion.AddRecord
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFMutualExclusion::AddRecord


## -description



Adds a record to the mutual exclusion object. A record specifies streams that are mutually exclusive with the streams in all other records.




## -parameters




### -param pdwRecordNumber [out]

Receives the index assigned to the new record. Record indexes are zero-based and sequential.


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



A record can include one or more stream numbers. All of the streams in a record are mutually exclusive with all the streams in all other records in the ASF mutual exclusion object.

You can use records to create complex mutual exclusion scenarios by using multiple ASF mutual exclusion objects.




## -see-also




<a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a>



<a href="https://msdn.microsoft.com/ecfb5e10-5102-4f6a-b67b-ba0ed06d0ed8">IMFASFMutualExclusion::RemoveRecord</a>



<a href="https://msdn.microsoft.com/fdd31eac-1dd6-45f0-90fb-d5a74c85db2e">Using Mutual Exclusion for ASF Streams</a>
 

 

