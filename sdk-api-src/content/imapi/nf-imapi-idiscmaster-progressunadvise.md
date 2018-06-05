---
UID: NF:imapi.IDiscMaster.ProgressUnadvise
title: IDiscMaster::ProgressUnadvise
author: windows-sdk-content
description: Cancels progress notifications for an application.
old-location: imapi\idiscmaster_progressunadvise.htm
old-project: imapi
ms.assetid: b2729ff7-aefb-40cf-ae7b-9451fbe10bbb
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IDiscMaster interface [IMAPI],ProgressUnadvise method, IDiscMaster.ProgressUnadvise, IDiscMaster::ProgressUnadvise, ProgressUnadvise, ProgressUnadvise method [IMAPI], ProgressUnadvise method [IMAPI],IDiscMaster interface, _win32_idiscmaster_progressunadvise, base.idiscmaster_progressunadvise, imapi.idiscmaster_progressunadvise, imapi/IDiscMaster::ProgressUnadvise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi.h
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
tech.root: 
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Actxprxy.dll
api_name:
-	IDiscMaster.ProgressUnadvise
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IDiscMaster::ProgressUnadvise


## -description


Cancels progress notifications for an application.


## -parameters




### -param vCookie






#### - nCookie [in]

Value returned by a previous call to the 
<a href="https://msdn.microsoft.com/64966230-2042-46cb-9974-adbe382723a1">ProgressAdvise</a> method.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/1473e79e-a13a-4bc5-b80d-d8921fdc9952">IDiscMaster</a>
 

 

