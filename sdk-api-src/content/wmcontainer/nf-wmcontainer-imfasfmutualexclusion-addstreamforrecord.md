---
UID: NF:wmcontainer.IMFASFMutualExclusion.AddStreamForRecord
title: IMFASFMutualExclusion::AddStreamForRecord
author: windows-sdk-content
description: Adds a stream number to a record in the Advanced Systems Format mutual exclusion object.
old-location: mf\imfasfmutualexclusion_addstreamforrecord.htm
old-project: medfound
ms.assetid: cfbfe3be-b0a4-408a-952e-e4f996f94cee
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: AddStreamForRecord, AddStreamForRecord method [Media Foundation], AddStreamForRecord method [Media Foundation],IMFASFMutualExclusion interface, IMFASFMutualExclusion interface [Media Foundation],AddStreamForRecord method, IMFASFMutualExclusion.AddStreamForRecord, IMFASFMutualExclusion::AddStreamForRecord, cfbfe3be-b0a4-408a-952e-e4f996f94cee, mf.imfasfmutualexclusion_addstreamforrecord, wmcontainer/IMFASFMutualExclusion::AddStreamForRecord
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
req.typenames: MFSINK_WMDRMACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFMutualExclusion.AddStreamForRecord
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFMutualExclusion::AddStreamForRecord


## -description



Adds a stream number to a record in the Advanced Systems Format mutual exclusion object.




## -parameters




### -param dwRecordNumber [in]

The record number to which the stream is added. A record number is set by the <a href="https://msdn.microsoft.com/f5dedc87-a29c-4c8d-b493-486d975f9ac4">IMFASFMutualExclusion::AddRecord</a> method.


### -param wStreamNumber [in]

The stream number to add to the record.


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
The specified stream number is already associated with the record.

</td>
</tr>
</table>
 




## -remarks



Each record includes one or more streams. Every stream in a record is mutually exclusive of all streams in every other record.




## -see-also




<a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a>



<a href="https://msdn.microsoft.com/ce410ae9-d0d0-4617-8178-829ef3c77ce0">IMFASFMutualExclusion::GetStreamsForRecord</a>



<a href="https://msdn.microsoft.com/d92c022c-3241-4296-9572-62b43c6e79cb">IMFASFMutualExclusion::RemoveStreamFromRecord</a>



<a href="https://msdn.microsoft.com/fdd31eac-1dd6-45f0-90fb-d5a74c85db2e">Using Mutual Exclusion for ASF Streams</a>
 

 

