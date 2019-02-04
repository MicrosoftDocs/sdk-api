---
UID: NF:dskquota.IDiskQuotaUser.Invalidate
title: IDiskQuotaUser::Invalidate
author: windows-sdk-content
description: Invalidates the quota information stored in the quota user object.
old-location: fs\idiskquotauser_invalidate.htm
tech.root: FileIO
ms.assetid: 23a51df4-0578-43fe-99cd-491f709accab
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiskQuotaUser interface [Files],Invalidate method, IDiskQuotaUser.Invalidate, IDiskQuotaUser::Invalidate, Invalidate, Invalidate method [Files], Invalidate method [Files],IDiskQuotaUser interface, _win32_idiskquotauser_invalidate, base.idiskquotauser_invalidate, dskquota/IDiskQuotaUser::Invalidate, fs.idiskquotauser_invalidate
ms.topic: method
req.header: dskquota.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Dskquota.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IDiskQuotaUser.Invalidate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaUser::Invalidate


## -description


Invalidates the quota information stored in the quota user object. The next time information is requested, it is refreshed from disk.


## -parameters






## -returns



This method returns <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a>
 

 

