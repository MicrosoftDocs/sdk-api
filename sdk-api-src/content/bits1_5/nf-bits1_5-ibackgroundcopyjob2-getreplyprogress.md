---
UID: NF:bits1_5.IBackgroundCopyJob2.GetReplyProgress
title: IBackgroundCopyJob2::GetReplyProgress
author: windows-sdk-content
description: Retrieves progress information related to the transfer of the reply data from an upload-reply job.
old-location: bits\ibackgroundcopyjob2_getreplyprogress.htm
old-project: Bits
ms.assetid: 76509b1a-fdfb-4236-8554-f63282bfc1b6
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetReplyProgress, GetReplyProgress method [BITS], GetReplyProgress method [BITS],IBackgroundCopyJob2 interface, IBackgroundCopyJob2 interface [BITS],GetReplyProgress method, IBackgroundCopyJob2.GetReplyProgress, IBackgroundCopyJob2::GetReplyProgress, _drz_ibackgroundcopyjob2_getreplyprogress, bits.ibackgroundcopyjob2_getreplyprogress, bits1_5/IBackgroundCopyJob2::GetReplyProgress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits1_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits1_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BG_AUTH_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	BitsPrx2.dll
api_name:
-	IBackgroundCopyJob2.GetReplyProgress
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: BitsPrx2.dll
req.irql: 
---

# IBackgroundCopyJob2::GetReplyProgress


## -description


Retrieves progress information related to the transfer of the reply data from an upload-reply job. 


## -parameters




### -param pProgress [out]

Contains information that you use to calculate the percentage of the reply file transfer that is complete. For more information, see 
<a href="https://msdn.microsoft.com/ea78ee22-87b2-4859-bd49-dd309c8aa234">BG_JOB_REPLY_PROGRESS</a>.


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
Progress information was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented for jobs of type <b>BG_JOB_TYPE_DOWNLOAD</b> or <b>BG_JOB_TYPE_UPLOAD</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pProgress</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/92c5d1d6-1e0b-4b92-9dc5-ec9a4e2c4649">BG_JOB_REPLY_PROGRESS</a>
 

 

