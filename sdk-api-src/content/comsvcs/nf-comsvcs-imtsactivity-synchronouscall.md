---
UID: NF:comsvcs.IMTSActivity.SynchronousCall
title: IMTSActivity::SynchronousCall
author: windows-sdk-content
description: Performs the user-defined work synchronously.
old-location: cos\imtsactivity_synchronouscall.htm
old-project: cossdk
ms.assetid: 4f69956b-fdb3-47c4-9a19-e9f39a8d5e06
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IMTSActivity interface [COM+],SynchronousCall method, IMTSActivity.SynchronousCall, IMTSActivity::SynchronousCall, SynchronousCall, SynchronousCall method [COM+], SynchronousCall method [COM+],IMTSActivity interface, _cos_IMTSActivity_SynchronousCall, comsvcs/IMTSActivity::SynchronousCall, cos.imtsactivity_synchronouscall
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
-	IMTSActivity.SynchronousCall
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMTSActivity::SynchronousCall


## -description


Performs the user-defined work synchronously.


## -parameters




### -param pCall [in]

A pointer to the <a href="https://msdn.microsoft.com/dccf53c3-19d9-435b-91b7-98e41bd48e29">IMTSCall</a> interface that is used to implement the batch work.


## -returns



This method always returns the <b>HRESULT</b> returned by the <a href="https://msdn.microsoft.com/410ed66e-db55-41e6-8f09-df4fe3aad3f2">OnCall</a> method of the <a href="https://msdn.microsoft.com/dccf53c3-19d9-435b-91b7-98e41bd48e29">IMTSCall</a> interface.





## -remarks



The batch work that is run using this method runs in the context and thread apartment of the activity that was created by the call to <a href="https://msdn.microsoft.com/25ae1f2e-f937-4d06-9709-ded2fc8c5777">MTSCreateActivity</a>.





## -see-also




<a href="https://msdn.microsoft.com/a45b29f0-d3f1-4593-9df5-4f6d617b93fa">IMTSActivity</a>
 

 

