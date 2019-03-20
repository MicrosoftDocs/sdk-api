---
UID: NF:wmcontainer.IMFASFMutualExclusion.GetRecordCount
title: IMFASFMutualExclusion::GetRecordCount (wmcontainer.h)
author: windows-sdk-content
description: Retrieves the number of records in the Advanced Systems Format mutual exclusion object.
old-location: mf\imfasfmutualexclusion_getrecordcount.htm
tech.root: medfound
ms.assetid: 8dbd883e-4ae3-422d-bb2e-087a9e311558
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 8dbd883e-4ae3-422d-bb2e-087a9e311558, GetRecordCount, GetRecordCount method [Media Foundation], GetRecordCount method [Media Foundation],IMFASFMutualExclusion interface, IMFASFMutualExclusion interface [Media Foundation],GetRecordCount method, IMFASFMutualExclusion.GetRecordCount, IMFASFMutualExclusion::GetRecordCount, mf.imfasfmutualexclusion_getrecordcount, wmcontainer/IMFASFMutualExclusion::GetRecordCount
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
 - IMFASFMutualExclusion.GetRecordCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFMutualExclusion::GetRecordCount


## -description



Retrieves the number of records in the Advanced Systems Format mutual exclusion object.




## -parameters




### -param pdwRecordCount [out]

Receives the count of records.


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



Each record includes one or more streams. Every stream in a record is mutually exclusive of streams in every other record.

Use this method in conjunction with <a href="https://msdn.microsoft.com/ce410ae9-d0d0-4617-8178-829ef3c77ce0">IMFASFMutualExclusion::GetStreamsForRecord</a> to retrieve the streams that are included in each record.




## -see-also




<a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a>



<a href="https://msdn.microsoft.com/f5dedc87-a29c-4c8d-b493-486d975f9ac4">IMFASFMutualExclusion::AddRecord</a>



<a href="https://msdn.microsoft.com/ce410ae9-d0d0-4617-8178-829ef3c77ce0">IMFASFMutualExclusion::GetStreamsForRecord</a>



<a href="https://msdn.microsoft.com/ecfb5e10-5102-4f6a-b67b-ba0ed06d0ed8">IMFASFMutualExclusion::RemoveRecord</a>



<a href="https://msdn.microsoft.com/fdd31eac-1dd6-45f0-90fb-d5a74c85db2e">Using Mutual Exclusion for ASF Streams</a>
 

 

