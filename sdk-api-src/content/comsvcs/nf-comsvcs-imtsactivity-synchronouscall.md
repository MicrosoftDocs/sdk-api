---
UID: NF:comsvcs.IMTSActivity.SynchronousCall
title: IMTSActivity::SynchronousCall
author: windows-sdk-content
description: Performs the user-defined work synchronously.
old-location: cos\imtsactivity_synchronouscall.htm
tech.root: cossdk
ms.assetid: 4f69956b-fdb3-47c4-9a19-e9f39a8d5e06
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMTSActivity interface [COM+],SynchronousCall method, IMTSActivity.SynchronousCall, IMTSActivity::SynchronousCall, SynchronousCall, SynchronousCall method [COM+], SynchronousCall method [COM+],IMTSActivity interface, _cos_IMTSActivity_SynchronousCall, comsvcs/IMTSActivity::SynchronousCall, cos.imtsactivity_synchronouscall
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IMTSActivity.SynchronousCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMTSActivity::SynchronousCall


## -description


Performs the user-defined work synchronously.


## -parameters




### -param pCall [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms687002(v=VS.85).aspx">IMTSCall</a> interface that is used to implement the batch work.


## -returns



This method always returns the <b>HRESULT</b> returned by the <a href="https://msdn.microsoft.com/410ed66e-db55-41e6-8f09-df4fe3aad3f2">OnCall</a> method of the <a href="https://msdn.microsoft.com/en-us/library/ms687002(v=VS.85).aspx">IMTSCall</a> interface.





## -remarks



The batch work that is run using this method runs in the context and thread apartment of the activity that was created by the call to <a href="https://msdn.microsoft.com/en-us/library/ms679476(v=VS.85).aspx">MTSCreateActivity</a>.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms685105(v=VS.85).aspx">IMTSActivity</a>
 

 

