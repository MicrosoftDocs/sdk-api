---
UID: NF:wcmconfig.IItemEnumerator.Reset
title: IItemEnumerator::Reset method
author: windows-driver-content
description: Resets the state of the enumerator to its initialized state. You must immediately follow IItemEnumerator::Reset with a call to IItemEnumerator::MoveNext on the enumerator in order to set the current pointer at the first position in the enumeration.
old-location: smi\iitemenumerator_reset.htm
old-project: SMI
ms.assetid: 6da5d581-7f8c-48fa-8522-1e51a805ad9b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IItemEnumerator, IItemEnumerator interface [SMI], Reset method, IItemEnumerator::Reset, Reset method [SMI], Reset method [SMI], IItemEnumerator interface, Reset,IItemEnumerator.Reset, smi.iitemenumerator_reset, wcmconfig/IItemEnumerator::Reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WcmNamespaceAccess
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SMIEngine.dll
api_name:
-	IItemEnumerator.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IItemEnumerator::Reset method


## -description


Resets the state of the enumerator to its initialized state. You must immediately follow <b>IItemEnumerator::Reset</b> with a call  to  <a href="https://msdn.microsoft.com/bdec3ee4-e66a-4e93-9109-c5721d06eb63">IItemEnumerator::MoveNext</a> on the enumerator   in order to set the current pointer at the first position in the enumeration.


## -parameters






## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success.




## -see-also




<a href="https://msdn.microsoft.com/f43245f1-81d9-4b06-8f0c-d490618a99fa">IItemEnumerator</a>
 

 

