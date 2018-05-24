---
UID: NF:faxcomex.IFaxIncomingQueue.put_Blocked
title: IFaxIncomingQueue::put_Blocked
author: windows-driver-content
description: The Blocked property is a Boolean value that indicates whether the job queue for incoming faxes is blocked.
old-location: fax\_mfax_faxincomingqueue_blocked_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_2rac.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: Blocked property [Fax Service], Blocked property [Fax Service],FaxIncomingQueue object, FaxIncomingQueue object [Fax Service],Blocked property, FaxIncomingQueue.Blocked, IFaxIncomingQueue.put_Blocked, IFaxIncomingQueue::put_Blocked, _mfax_faxincomingqueue.blocked, fax._mfax_faxincomingqueue_blocked, fax._mfax_faxincomingqueue_blocked_vb, put_Blocked
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	FaxIncomingQueue.Blocked
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxIncomingQueue::put_Blocked


## -description


The <b>Blocked</b> property is a Boolean value that indicates whether the job queue for incoming faxes is blocked. 

This property is read/write.


## -parameters


## -remarks



If this property is equal to <b>True</b>, the inbound job queue is blocked and the fax service is not answering incoming fax calls. If this property is equal to <b>False</b>, the queue is not blocked.




## -see-also




<a href="https://msdn.microsoft.com/769e4fc5-5607-4fd6-8f78-59b190c94787">FaxIncomingQueue</a>



<a href="https://msdn.microsoft.com/291f8709-c10f-4041-864f-82431edd7fab">IFaxIncomingQueue</a>
 

 

