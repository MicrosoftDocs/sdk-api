---
UID: NF:bits.IEnumBackgroundCopyJobs.Clone
title: IEnumBackgroundCopyJobs::Clone (bits.h)
author: windows-sdk-content
description: Creates another IEnumBackgroundCopyJobs enumerator that contains the same enumeration state as the current one.
old-location: bits\ienumbackgroundcopyjobs_clone.htm
tech.root: Bits
ms.assetid: 5d83af74-c24c-41e2-aef4-d7210a1d0160
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [BITS], Clone method [BITS],IEnumBackgroundCopyJobs interface, IEnumBackgroundCopyJobs interface [BITS],Clone method, IEnumBackgroundCopyJobs.Clone, IEnumBackgroundCopyJobs::Clone, _drz_ienumbackgroundcopyjobs_clone, bits.ienumbackgroundcopyjobs_clone, bits/IEnumBackgroundCopyJobs::Clone
ms.topic: method
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IEnumBackgroundCopyJobs.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumBackgroundCopyJobs::Clone


## -description


Creates another 
<a href="https://msdn.microsoft.com/21ff88da-9fae-478f-bcba-488ed7a89608">IEnumBackgroundCopyJobs</a> enumerator that contains the same enumeration state as the current one.

Using this method, a client can record a particular point in the enumeration sequence, and then return to that point at a later time. The new enumerator supports the same interface as the original one.


## -parameters




### -param ppenum [out]

Receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined. You must release <i>ppEnumJobs</i> when done.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://msdn.microsoft.com/21ff88da-9fae-478f-bcba-488ed7a89608">IEnumBackgroundCopyJobs</a>
 

 

