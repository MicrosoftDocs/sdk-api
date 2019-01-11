---
UID: NF:qmgr.IEnumBackgroundCopyGroups.Clone
title: IEnumBackgroundCopyGroups::Clone
author: windows-sdk-content
description: Use the Clone method to create another IEnumBackgroundCopyGroups enumerator that contains the same enumeration state as the current one.
old-location: bits\ienumbackgroundcopygroups_clone.htm
tech.root: Bits
ms.assetid: f2743edd-9fc5-451b-b1ff-17f4591923ba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [BITS], Clone method [BITS],IEnumBackgroundCopyGroups interface, IEnumBackgroundCopyGroups interface [BITS],Clone method, IEnumBackgroundCopyGroups.Clone, IEnumBackgroundCopyGroups::Clone, bits.ienumbackgroundcopygroups_clone, qmgr/IEnumBackgroundCopyGroups::Clone
ms.topic: method
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
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
 - IEnumBackgroundCopyGroups.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumBackgroundCopyGroups::Clone


## -description


<p class="CCE_Message">[<b>IEnumBackgroundCopyGroups</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>Clone</b> method to create another <a href="https://msdn.microsoft.com/64a05103-9749-41fd-9987-8bb17b9284f7">IEnumBackgroundCopyGroups</a> enumerator that contains the same enumeration state as the current one. 



Using this method, a client can record a particular point in the enumeration sequence, and then return to that point at a later time. The new enumerator supports the same interface as the original one.


## -parameters




### -param ppenum [out]

Receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined. You must release <i>ppenum</i> when done.


## -returns



This method returns <b>S_OK</b> on success.




## -see-also




<a href="https://msdn.microsoft.com/64a05103-9749-41fd-9987-8bb17b9284f7">IEnumBackgroundCopyGroups</a>
 

 

