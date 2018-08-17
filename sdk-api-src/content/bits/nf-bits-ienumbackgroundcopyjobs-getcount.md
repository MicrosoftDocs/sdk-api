---
UID: NF:bits.IEnumBackgroundCopyJobs.GetCount
title: IEnumBackgroundCopyJobs::GetCount
author: windows-sdk-content
description: Retrieves a count of the number of jobs in the enumeration.
old-location: bits\ienumbackgroundcopyjobs_getcount.htm
old-project: bits
ms.assetid: 024ffd11-5084-4ff5-b1b6-9aec3e802900
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetCount, GetCount method [BITS], GetCount method [BITS],IEnumBackgroundCopyJobs interface, IEnumBackgroundCopyJobs interface [BITS],GetCount method, IEnumBackgroundCopyJobs.GetCount, IEnumBackgroundCopyJobs::GetCount, _drz_ienumbackgroundcopyjobs_getcount, bits.ienumbackgroundcopyjobs_getcount, bits/IEnumBackgroundCopyJobs::GetCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IEnumBackgroundCopyJobs.GetCount
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IEnumBackgroundCopyJobs::GetCount


## -description


Retrieves a count of the number of jobs in the enumeration.


## -parameters




### -param puCount






#### - pCount [out]

Number of jobs in the enumeration.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa363109(v=VS.85).aspx">IEnumBackgroundCopyJobs</a>
 

 

