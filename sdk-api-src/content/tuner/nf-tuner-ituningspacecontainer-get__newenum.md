---
UID: NF:tuner.ITuningSpaceContainer.get__NewEnum
title: ITuningSpaceContainer::get__NewEnum method
author: windows-driver-content
description: The get__NewEnum method supports For...Each loops in Automation clients.
old-location: mstv\ituningspacecontainer_get__newenum.htm
old-project: mstv
ms.assetid: f2bcd80b-b36c-44b1-9a87-beda7ae12117
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITuningSpaceContainer, ITuningSpaceContainer interface [Microsoft TV Technologies], get__NewEnum method, ITuningSpaceContainer::get__NewEnum, ITuningSpaceContainerget__NewEnum, get__NewEnum method [Microsoft TV Technologies], get__NewEnum method [Microsoft TV Technologies], ITuningSpaceContainer interface, get__NewEnum,ITuningSpaceContainer.get__NewEnum, mstv.ituningspacecontainer_get__newenum, tuner/ITuningSpaceContainer::get__NewEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	ITuningSpaceContainer.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpaceContainer::get__NewEnum method


## -description



The <b>get__NewEnum</b> method supports <code>For...Each</code> loops in Automation clients.




## -parameters




### -param NewEnum






#### - ppNewEnum [out]

Pointer to a variable that receives an <b>IEnumVARIANT</b> interface pointer. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method is provided to enable scripting and Visual Basic  applications to iterate through the collection in a <code>For...Each</code> loop. C++ applications should use the <a href="https://msdn.microsoft.com/7cd6a691-8c47-4c26-8afd-57f6965246ff">ITuningSpaceContainer::get_EnumTuningSpaces</a> method.

The returned <b>IEnumVARIANT</b> interface is not thread safe, because it is intended primarily for use by Automation clients. Clients should not call methods on the interface from more than one thread.




## -see-also




<a href="https://msdn.microsoft.com/8f053c53-2a2b-4d98-a510-c516faa21611">ITuningSpaceContainer Interface</a>
 

 

