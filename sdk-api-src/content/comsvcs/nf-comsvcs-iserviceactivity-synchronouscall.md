---
UID: NF:comsvcs.IServiceActivity.SynchronousCall
title: IServiceActivity::SynchronousCall method
author: windows-driver-content
description: Performs the user-defined work synchronously.
old-location: cos\iserviceactivity_synchronouscall.htm
old-project: cossdk
ms.assetid: d25e6942-7b1b-4b74-b711-2d0f513d0b38
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IServiceActivity, IServiceActivity interface [COM+], SynchronousCall method, IServiceActivity::SynchronousCall, SynchronousCall method [COM+], SynchronousCall method [COM+], IServiceActivity interface, SynchronousCall,IServiceActivity.SynchronousCall, _cos_IServiceActivity_SynchronousCall, comsvcs/IServiceActivity::SynchronousCall, cos.iserviceactivity_synchronouscall
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IServiceActivity.SynchronousCall
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceActivity::SynchronousCall method


## -description


Performs the user-defined work synchronously.


## -parameters




### -param pIServiceCall [in]

A pointer to the <a href="https://msdn.microsoft.com/97532e29-3d1a-4a7c-8103-dd7ae2866a70">IServiceCall</a> interface that is used to implement the batch work.


## -returns



This method always returns the <b>HRESULT</b> value returned by the <a href="https://msdn.microsoft.com/0a2bb7ed-018f-4cb1-a1b2-27f6949dae39">OnCall</a> method of the <a href="https://msdn.microsoft.com/97532e29-3d1a-4a7c-8103-dd7ae2866a70">IServiceCall</a> interface.





## -remarks



The batch work that is run via this method runs in the context and thread apartment of the activity created by the call to <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>.





## -see-also




<a href="https://msdn.microsoft.com/005bf0ec-f5a7-41a3-85b3-07f79f26af27">IServiceActivity</a>
 

 

