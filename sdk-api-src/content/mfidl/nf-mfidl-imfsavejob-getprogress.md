---
UID: NF:mfidl.IMFSaveJob.GetProgress
title: IMFSaveJob::GetProgress
author: windows-driver-content
description: Retrieves the percentage of content saved to the provided byte stream.
old-location: mf\imfsavejob_getprogress.htm
old-project: medfound
ms.assetid: 8782333c-796c-4401-9575-c78e95887015
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: 8782333c-796c-4401-9575-c78e95887015, GetProgress, GetProgress method [Media Foundation], GetProgress method [Media Foundation],IMFSaveJob interface, IMFSaveJob interface [Media Foundation],GetProgress method, IMFSaveJob.GetProgress, IMFSaveJob::GetProgress, mf.imfsavejob_getprogress, mfidl/IMFSaveJob::GetProgress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFSaveJob.GetProgress
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSaveJob::GetProgress


## -description



Retrieves the percentage of content saved to the provided byte stream.




## -parameters




### -param pdwPercentComplete [out]

Receives the percentage of completion.


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




<a href="https://msdn.microsoft.com/0f38fa60-ed04-40c4-9bb0-b6e196cd9586">IMFSaveJob</a>
 

 

