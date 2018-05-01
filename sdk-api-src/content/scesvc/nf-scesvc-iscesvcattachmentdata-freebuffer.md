---
UID: NF:scesvc.ISceSvcAttachmentData.FreeBuffer
title: ISceSvcAttachmentData::FreeBuffer method
author: windows-driver-content
description: The FreeBuffer method frees memory allocated by the Security Configuration snap-in.
old-location: security\iscesvcattachmentdata_freebuffer.htm
old-project: SecMgmt
ms.assetid: 3645547e-5d6e-42df-802b-cf8b1a4c1e11
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: FreeBuffer method [Security], FreeBuffer method [Security], ISceSvcAttachmentData interface, FreeBuffer,ISceSvcAttachmentData.FreeBuffer, ISceSvcAttachmentData, ISceSvcAttachmentData interface [Security], FreeBuffer method, ISceSvcAttachmentData::FreeBuffer, _config_iscesvcattachmentdata_freebuffer, scesvc/ISceSvcAttachmentData::FreeBuffer, security.iscesvcattachmentdata_freebuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: scesvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SCESVC_INFO_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsecedit.dll
api_name:
-	ISceSvcAttachmentData.FreeBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsecedit.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISceSvcAttachmentData::FreeBuffer method


## -description


The <b>FreeBuffer</b> method frees memory allocated by the Security Configuration snap-in.


## -parameters




### -param pvData [in]

Void pointer to the buffer to be freed.


## -returns



The return value is an HRESULT. A value of S_OK indicates the method was successful.




## -remarks



You should call this method to free the data buffer returned by 
<a href="https://msdn.microsoft.com/f0b51592-58d9-45f2-a0a5-7cdbde0bc0a1">ISceSvcAttachmentData::GetData</a>.




## -see-also




<a href="https://msdn.microsoft.com/385acdb9-5642-47c1-b2ac-be388edaac12">ISceSvcAttachmentData</a>



<a href="https://msdn.microsoft.com/f0b51592-58d9-45f2-a0a5-7cdbde0bc0a1">ISceSvcAttachmentData::GetData</a>
 

 

