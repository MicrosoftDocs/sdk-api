---
UID: NF:ktmw32.CommitEnlistment
title: CommitEnlistment function (ktmw32.h)
author: windows-sdk-content
description: Commits the transaction associated with this enlistment handle. This function is used by communication resource managers (sometimes called superior transaction managers).
old-location: fs\commitenlistment.htm
tech.root: ktm
ms.assetid: d1e1043d-2db3-4f05-affc-2d32744baf10
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CommitEnlistment, CommitEnlistment function [Files], fs.commitenlistment, ktmw32/CommitEnlistment
ms.topic: function
req.header: ktmw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
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
req.lib: KtmW32.lib
req.dll: KtmW32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - KtmW32.dll
api_name:
 - CommitEnlistment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CommitEnlistment function


## -description


Commits the transaction associated with this enlistment handle. This function is used by communication 
    resource managers (sometimes called superior transaction managers).


## -parameters




### -param EnlistmentHandle [in]

A handle to the enlistment to commit.


### -param TmVirtualClock [in]

A pointer to the latest virtual clock value received for this enlistment. If you specify 
      <b>NULL</b>, the virtual clock value is not changed.

To change the virtual clock value, this value must be greater than the current value returned by a 
      subordinate TM.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.


The following list identifies the possible error codes:






## -see-also




<a href="https://msdn.microsoft.com/de3e3a26-3e56-4732-8e7c-945b45593aed">CommitComplete</a>



<a href="https://msdn.microsoft.com/7bc06468-947f-48ec-8e58-20df58ed93bd">CreateEnlistment</a>



<a href="https://msdn.microsoft.com/21d7c0fa-3a49-43b3-9325-d3dfdabbcb98">GetCurrentClockTransactionManager</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

