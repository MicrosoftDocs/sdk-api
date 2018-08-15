---
UID: NF:wsbapp.IWsbApplicationAsync.Abort
title: IWsbApplicationAsync::Abort
author: windows-sdk-content
description: Cancels an incomplete asynchronous operation.
old-location: wsb\iwsbapplicationasync_abort.htm
old-project: wsb
ms.assetid: 937ca809-4bb0-408e-9c7e-eccc43d8d4ae
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Abort, Abort method [Windows Server Backup], Abort method [Windows Server Backup],IWsbApplicationAsync interface, IWsbApplicationAsync interface [Windows Server Backup],Abort method, IWsbApplicationAsync.Abort, IWsbApplicationAsync::Abort, wsb.iwsbapplicationasync_abort, wsbapp/IWsbApplicationAsync::Abort
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsbapp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WSPUPCALLTABLE, *LPWSPUPCALLTABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WsbApp.h
api_name:
 - IWsbApplicationAsync.Abort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWsbApplicationAsync::Abort


## -description


Cancels an incomplete asynchronous operation.


## -parameters






## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



Windows Server Backup calls this method to cancel an asynchronous operation. For example, if the overall backup operation is canceled while an asynchronous consistency-check operation is in progress, this method will be called to cancel the consistency-check operation.




## -see-also




<a href="https://msdn.microsoft.com/cd8f74c0-c2dc-487c-b702-1e1355e99b7d">IWsbApplicationAsync</a>
 

 

