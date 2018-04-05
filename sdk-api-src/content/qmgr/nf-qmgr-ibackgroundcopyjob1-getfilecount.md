---
UID: NF:qmgr.IBackgroundCopyJob1.GetFileCount
title: IBackgroundCopyJob1::GetFileCount method
author: windows-driver-content
description: Use the GetFileCount method to retrieve the number of files in the job.
old-location: bits\ibackgroundcopyjob1_getfilecount.htm
old-project: Bits
ms.assetid: 6aec5e9c-2950-4039-99a4-b1884a9a4673
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetFileCount method [BITS], GetFileCount method [BITS], IBackgroundCopyJob1 interface, GetFileCount,IBackgroundCopyJob1.GetFileCount, IBackgroundCopyJob1, IBackgroundCopyJob1 interface [BITS], GetFileCount method, IBackgroundCopyJob1::GetFileCount, bits.ibackgroundcopyjob1_getfilecount, qmgr/IBackgroundCopyJob1::GetFileCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: GROUPPROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IBackgroundCopyJob1.GetFileCount
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IBackgroundCopyJob1::GetFileCount method


## -description


<p class="CCE_Message">[<b>IBackgroundCopyJob1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>GetFileCount</b> method to retrieve the number of files in the job.


## -parameters




### -param pdwFileCount [out]

Number of files in the job.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully retrieved the number of files in the job.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ccf1b355-c1af-4b5e-b613-181c426ed777">IBackgroundCopyJob1</a>
 

 

