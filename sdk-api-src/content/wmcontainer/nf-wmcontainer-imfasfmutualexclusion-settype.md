---
UID: NF:wmcontainer.IMFASFMutualExclusion.SetType
title: IMFASFMutualExclusion::SetType
author: windows-sdk-content
description: Sets the type of mutual exclusion that is represented by the Advanced Systems Format (ASF) mutual exclusion object.
old-location: mf\imfasfmutualexclusion_settype.htm
old-project: medfound
ms.assetid: 58fc1c27-0a7d-48bb-b5a4-ab299c5e0ac6
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 58fc1c27-0a7d-48bb-b5a4-ab299c5e0ac6, IMFASFMutualExclusion interface [Media Foundation],SetType method, IMFASFMutualExclusion.SetType, IMFASFMutualExclusion::SetType, SetType, SetType method [Media Foundation], SetType method [Media Foundation],IMFASFMutualExclusion interface, mf.imfasfmutualexclusion_settype, wmcontainer/IMFASFMutualExclusion::SetType
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
 - IMFASFMutualExclusion.SetType
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFMutualExclusion::SetType


## -description



Sets the type of mutual exclusion that is represented by the Advanced Systems Format (ASF) mutual exclusion object.




## -parameters




### -param guidType [in]

The type of mutual exclusion that is represented by the ASF mutual exclusion object. For a list of predefined mutual exclusion type constants, see <a href="https://msdn.microsoft.com/3db8eebd-2e26-4c77-8f66-7d08436c9e42">ASF Mutual Exclusion Type GUIDs</a>.


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



Sometimes, content must be made mutually exclusive in more than one way. For example, a video file might contain audio streams in several bit rates for each of several languages. To handle this type of complex mutual exclusion, you must configure more than one ASF mutual exclusion object. For more information, see <a href="https://msdn.microsoft.com/f5dedc87-a29c-4c8d-b493-486d975f9ac4">IMFASFMutualExclusion::AddRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a>



<a href="https://msdn.microsoft.com/c6af870e-2ef8-4dea-b76b-7a78ceaaa3d3">IMFASFMutualExclusion::GetType</a>



<a href="https://msdn.microsoft.com/fdd31eac-1dd6-45f0-90fb-d5a74c85db2e">Using Mutual Exclusion for ASF Streams</a>
 

 

