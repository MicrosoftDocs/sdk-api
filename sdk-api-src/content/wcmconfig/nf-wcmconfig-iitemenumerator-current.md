---
UID: NF:wcmconfig.IItemEnumerator.Current
title: IItemEnumerator::Current
author: windows-sdk-content
description: Retrieves an item from the current position of the enumerator.
old-location: smi\iitemenumerator_current.htm
old-project: SMI
ms.assetid: 0f117274-672f-40da-a4c6-88dd6aa01cf7
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Current, Current method [SMI], Current method [SMI],IItemEnumerator interface, IItemEnumerator interface [SMI],Current method, IItemEnumerator.Current, IItemEnumerator::Current, smi.iitemenumerator_current, wcmconfig/IItemEnumerator::Current
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WcmNamespaceAccess
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - IItemEnumerator.Current
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IItemEnumerator::Current


## -description


Retrieves an item from the current position of the enumerator.


## -parameters




### -param Item [out]

A variant that contains the key value for the collection. For most collections, the key is the name of the item.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success.




## -remarks



<div class="alert"><b>Note</b>  When the item is no longer required, call <a href="https://msdn.microsoft.com/library/ms221165(v=VS.85).aspx">VariantClear</a> to free the resources associated with the item.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f43245f1-81d9-4b06-8f0c-d490618a99fa">IItemEnumerator</a>
 

 

