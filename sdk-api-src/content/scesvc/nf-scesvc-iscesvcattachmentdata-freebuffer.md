---
UID: NF:scesvc.ISceSvcAttachmentData.FreeBuffer
title: ISceSvcAttachmentData::FreeBuffer (scesvc.h)
author: windows-sdk-content
description: The FreeBuffer method frees memory allocated by the Security Configuration snap-in.
old-location: security\iscesvcattachmentdata_freebuffer.htm
tech.root: SecMgmt
ms.assetid: 3645547e-5d6e-42df-802b-cf8b1a4c1e11
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FreeBuffer, FreeBuffer method [Security], FreeBuffer method [Security],ISceSvcAttachmentData interface, ISceSvcAttachmentData interface [Security],FreeBuffer method, ISceSvcAttachmentData.FreeBuffer, ISceSvcAttachmentData::FreeBuffer, _config_iscesvcattachmentdata_freebuffer, scesvc/ISceSvcAttachmentData::FreeBuffer, security.iscesvcattachmentdata_freebuffer
ms.topic: method
f1_keywords: 
 - "scesvc/ISceSvcAttachmentData.FreeBuffer"
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
req.lib: 
req.dll: Wsecedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsecedit.dll
api_name:
 - ISceSvcAttachmentData.FreeBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISceSvcAttachmentData::FreeBuffer


## -description


The <b>FreeBuffer</b> method frees memory allocated by the Security Configuration snap-in.


## -parameters




### -param pvData [in]

Void pointer to the buffer to be freed.


## -returns



The return value is an HRESULT. A value of S_OK indicates the method was successful.




## -remarks



You should call this method to free the data buffer returned by 
<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentdata-getdata">ISceSvcAttachmentData::GetData</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nn-scesvc-iscesvcattachmentdata">ISceSvcAttachmentData</a>



<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentdata-getdata">ISceSvcAttachmentData::GetData</a>
 

 

