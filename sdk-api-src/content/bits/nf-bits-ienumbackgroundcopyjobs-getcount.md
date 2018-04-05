---
UID: NF:bits.IEnumBackgroundCopyJobs.GetCount
title: IEnumBackgroundCopyJobs::GetCount method
author: windows-driver-content
description: Retrieves a count of the number of jobs in the enumeration.
old-location: bits\ienumbackgroundcopyjobs_getcount.htm
old-project: Bits
ms.assetid: 024ffd11-5084-4ff5-b1b6-9aec3e802900
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetCount method [BITS], GetCount method [BITS], IEnumBackgroundCopyJobs interface, GetCount,IEnumBackgroundCopyJobs.GetCount, IEnumBackgroundCopyJobs, IEnumBackgroundCopyJobs interface [BITS], GetCount method, IEnumBackgroundCopyJobs::GetCount, _drz_ienumbackgroundcopyjobs_getcount, bits.ienumbackgroundcopyjobs_getcount, bits/IEnumBackgroundCopyJobs::GetCount
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IEnumBackgroundCopyJobs.GetCount
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IEnumBackgroundCopyJobs::GetCount method


## -description


Retrieves a count of the number of jobs in the enumeration.


## -parameters




### -param puCount






#### - pCount [out]

Number of jobs in the enumeration.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://msdn.microsoft.com/21ff88da-9fae-478f-bcba-488ed7a89608">IEnumBackgroundCopyJobs</a>
 

 

