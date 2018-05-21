---
UID: NE:bits.__MIDL_IBackgroundCopyJob_0003
title: "__MIDL_IBackgroundCopyJob_0003"
author: windows-driver-content
description: The BG_JOB_TYPE enumeration defines constant values that specify the type of transfer job, such as download.
old-location: bits\bg_job_type.htm
old-project: Bits
ms.assetid: b341a63f-3a1d-4518-8f05-17d28af603b4
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: BG_JOB_TYPE, BG_JOB_TYPE enumeration [BITS], BG_JOB_TYPE_DOWNLOAD, BG_JOB_TYPE_UPLOAD, BG_JOB_TYPE_UPLOAD_REPLY, __MIDL_IBackgroundCopyJob_0003, _drz_bg_job_type, bits.bg_job_type, bits/BG_JOB_TYPE, bits/BG_JOB_TYPE_DOWNLOAD, bits/BG_JOB_TYPE_UPLOAD, bits/BG_JOB_TYPE_UPLOAD_REPLY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BG_JOB_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Bits.h
api_name:
-	BG_JOB_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# __MIDL_IBackgroundCopyJob_0003 enumeration


## -description


The 
<b>BG_JOB_TYPE</b> enumeration defines constant values that specify the type of transfer job, such as download.


## -enum-fields




### -field BG_JOB_TYPE_DOWNLOAD

Specifies that the job downloads files to the client.


### -field BG_JOB_TYPE_UPLOAD

Specifies that the job uploads a file to the server. 

<b>BITS 1.2 and earlier:  </b>Not supported.


### -field BG_JOB_TYPE_UPLOAD_REPLY

Specifies that the job uploads a file to the server and receives a reply file from the server application. 

<b>BITS 1.2 and earlier:  </b>Not supported.


## -see-also




<a href="https://msdn.microsoft.com/b84c45c2-379a-40d0-91ab-0124f0ef6b00">IBackgroundCopyJob::GetType</a>



<a href="https://msdn.microsoft.com/6d23e3c0-673b-4f37-b6a0-e364b2d73886">IBackgroundCopyManager::CreateJob</a>
 

 

