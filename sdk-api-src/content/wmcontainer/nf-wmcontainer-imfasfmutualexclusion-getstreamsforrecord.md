---
UID: NF:wmcontainer.IMFASFMutualExclusion.GetStreamsForRecord
title: IMFASFMutualExclusion::GetStreamsForRecord
author: windows-sdk-content
description: Retrieves the stream numbers contained in a record in the Advanced Systems Format mutual exclusion object.
old-location: mf\imfasfmutualexclusion_getstreamsforrecord.htm
tech.root: medfound
ms.assetid: ce410ae9-d0d0-4617-8178-829ef3c77ce0
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetStreamsForRecord, GetStreamsForRecord method [Media Foundation], GetStreamsForRecord method [Media Foundation],IMFASFMutualExclusion interface, IMFASFMutualExclusion interface [Media Foundation],GetStreamsForRecord method, IMFASFMutualExclusion.GetStreamsForRecord, IMFASFMutualExclusion::GetStreamsForRecord, ce410ae9-d0d0-4617-8178-829ef3c77ce0, mf.imfasfmutualexclusion_getstreamsforrecord, wmcontainer/IMFASFMutualExclusion::GetStreamsForRecord
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
 - IMFASFMutualExclusion.GetStreamsForRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFMutualExclusion::GetStreamsForRecord


## -description



Retrieves the stream numbers contained in a record in the Advanced Systems Format mutual exclusion object.




## -parameters




### -param dwRecordNumber [in]

The number of the record for which to retrieve the stream numbers.


### -param pwStreamNumArray [out]

An array that receives the stream numbers. Set to <b>NULL</b> to get the number of elements required, which is indicated by the value of <i>pcStreams</i> on return. If this parameter is not <b>NULL</b>, the method will copy as many stream numbers to the array as there are elements indicated by the value of <i>pcStreams</i>.


### -param pcStreams [in, out]

On input, the number of elements in the array referenced by <i>pwStreamNumArray</i>. On output, the method sets this value to the count of stream numbers in the record. You can call <b>GetStreamsForRecord</b> with <i>pwStreamNumArray</i> set to <b>NULL</b> to retrieve the number of elements required to hold all of the stream numbers.


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
 




## -see-also




<a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a>



<a href="https://msdn.microsoft.com/fdd31eac-1dd6-45f0-90fb-d5a74c85db2e">Using Mutual Exclusion for ASF Streams</a>
 

 

