---
UID: NF:wmcontainer.IMFASFMutualExclusion.RemoveStreamFromRecord
title: IMFASFMutualExclusion::RemoveStreamFromRecord
author: windows-sdk-content
description: Removes a stream number from a record in the Advanced Systems Format mutual exclusion object.
old-location: mf\imfasfmutualexclusion_removestreamfromrecord.htm
tech.root: medfound
ms.assetid: d92c022c-3241-4296-9572-62b43c6e79cb
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: IMFASFMutualExclusion interface [Media Foundation],RemoveStreamFromRecord method, IMFASFMutualExclusion.RemoveStreamFromRecord, IMFASFMutualExclusion::RemoveStreamFromRecord, RemoveStreamFromRecord, RemoveStreamFromRecord method [Media Foundation], RemoveStreamFromRecord method [Media Foundation],IMFASFMutualExclusion interface, d92c022c-3241-4296-9572-62b43c6e79cb, mf.imfasfmutualexclusion_removestreamfromrecord, wmcontainer/IMFASFMutualExclusion::RemoveStreamFromRecord
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
 - IMFASFMutualExclusion.RemoveStreamFromRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFMutualExclusion::RemoveStreamFromRecord


## -description



Removes a stream number from a record in the Advanced Systems Format mutual exclusion object.




## -parameters




### -param dwRecordNumber [in]

The record number from which to remove the stream number.


### -param wStreamNumber [in]

The stream number to remove from the record.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The stream number is not listed for the specified record.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a>



<a href="https://msdn.microsoft.com/fdd31eac-1dd6-45f0-90fb-d5a74c85db2e">Using Mutual Exclusion for ASF Streams</a>
 

 

