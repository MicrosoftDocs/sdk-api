---
UID: NF:scesvc.ISceSvcAttachmentData.CloseHandle
title: ISceSvcAttachmentData::CloseHandle
author: windows-sdk-content
description: The CloseHandle method closes a handle opened during a previous call to ISceSvcAttachmentData::Initialize.
old-location: security\iscesvcattachmentdata_closehandle.htm
tech.root: secmgmt
ms.assetid: e50f5acf-06ef-49bb-bcf1-1fadeb4b808a
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CloseHandle, CloseHandle method [Security], CloseHandle method [Security],ISceSvcAttachmentData interface, ISceSvcAttachmentData interface [Security],CloseHandle method, ISceSvcAttachmentData.CloseHandle, ISceSvcAttachmentData::CloseHandle, _config_iscesvcattachmentdata_closehandle, scesvc/ISceSvcAttachmentData::CloseHandle, security.iscesvcattachmentdata_closehandle
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
 - ISceSvcAttachmentData.CloseHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISceSvcAttachmentData::CloseHandle


## -description


The <b>CloseHandle</b> method closes a handle opened during a previous call to 
<a href="https://msdn.microsoft.com/2c5d087d-774b-4cfb-a458-9a5b1c6106c7">ISceSvcAttachmentData::Initialize</a>.


## -parameters




### -param scesvcHandle [in]

The 
<a href="https://msdn.microsoft.com/478d7d4b-7983-4247-b8be-2e2cd3327533">SCESVC_HANDLE</a> to close.


## -returns



The return value is an <b>HRESULT</b>. A value of <b>S_OK</b> indicates the method was successful.




## -remarks



You should call this method when your attachment snap-in extension no longer requires the handle returned by 
<a href="https://msdn.microsoft.com/2c5d087d-774b-4cfb-a458-9a5b1c6106c7">ISceSvcAttachmentData::Initialize</a>.




## -see-also




<a href="https://msdn.microsoft.com/385acdb9-5642-47c1-b2ac-be388edaac12">ISceSvcAttachmentData</a>



<a href="https://msdn.microsoft.com/2c5d087d-774b-4cfb-a458-9a5b1c6106c7">ISceSvcAttachmentData::Initialize</a>
 

 

