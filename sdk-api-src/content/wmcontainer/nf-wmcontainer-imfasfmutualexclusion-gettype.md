---
UID: NF:wmcontainer.IMFASFMutualExclusion.GetType
title: IMFASFMutualExclusion::GetType
author: windows-sdk-content
description: Retrieves the type of mutual exclusion represented by the Advanced Systems Format (ASF) mutual exclusion object.
old-location: mf\imfasfmutualexclusion_gettype.htm
tech.root: medfound
ms.assetid: c6af870e-2ef8-4dea-b76b-7a78ceaaa3d3
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetType, GetType method [Media Foundation], GetType method [Media Foundation],IMFASFMutualExclusion interface, IMFASFMutualExclusion interface [Media Foundation],GetType method, IMFASFMutualExclusion.GetType, IMFASFMutualExclusion::GetType, c6af870e-2ef8-4dea-b76b-7a78ceaaa3d3, mf.imfasfmutualexclusion_gettype, wmcontainer/IMFASFMutualExclusion::GetType
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
 - IMFASFMutualExclusion.GetType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFMutualExclusion::GetType


## -description



Retrieves the type of mutual exclusion represented by the Advanced Systems Format (ASF) mutual exclusion object.




## -parameters




### -param pguidType [out]

A variable that receives the type identifier. For a list of predefined mutual exclusion type constants, see <a href="https://msdn.microsoft.com/3db8eebd-2e26-4c77-8f66-7d08436c9e42">ASF Mutual Exclusion Type GUIDs</a>.


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



Sometimes, content must be made mutually exclusive in more than one way. For example, a video file might contain audio streams of several bit rates for each of several languages. To handle this type of complex mutual exclusion, you must configure more than one ASF mutual exclusion object. For more information, see <a href="https://msdn.microsoft.com/f5dedc87-a29c-4c8d-b493-486d975f9ac4">IMFASFMutualExclusion::AddRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a>



<a href="https://msdn.microsoft.com/58fc1c27-0a7d-48bb-b5a4-ab299c5e0ac6">IMFASFMutualExclusion::SetType</a>



<a href="https://msdn.microsoft.com/fdd31eac-1dd6-45f0-90fb-d5a74c85db2e">Using Mutual Exclusion for ASF Streams</a>
 

 

