---
UID: NF:wmcontainer.IMFASFMutualExclusion.Clone
title: IMFASFMutualExclusion::Clone
author: windows-driver-content
description: Creates a copy of the Advanced Systems Format mutual exclusion object.
old-location: mf\imfasfmutualexclusion_clone.htm
old-project: medfound
ms.assetid: 32bd09d7-9d85-4692-8b2f-6afab3234fa9
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 32bd09d7-9d85-4692-8b2f-6afab3234fa9, Clone, Clone method [Media Foundation], Clone method [Media Foundation],IMFASFMutualExclusion interface, IMFASFMutualExclusion interface [Media Foundation],Clone method, IMFASFMutualExclusion.Clone, IMFASFMutualExclusion::Clone, mf.imfasfmutualexclusion_clone, wmcontainer/IMFASFMutualExclusion::Clone
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
-	IMFASFMutualExclusion.Clone
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFMutualExclusion::Clone


## -description



Creates a copy of the Advanced Systems Format mutual exclusion object.




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



The cloned object is a new object, completely independent of the object from which it was cloned.




## -see-also




<a href="https://msdn.microsoft.com/9c2278ec-77d1-445e-94bc-44e5d48f14ae">IMFASFMutualExclusion</a>



<a href="https://msdn.microsoft.com/fdd31eac-1dd6-45f0-90fb-d5a74c85db2e">Using Mutual Exclusion for ASF Streams</a>
 

 

