---
UID: NF:dskquota.IEnumDiskQuotaUsers.Skip
title: IEnumDiskQuotaUsers::Skip
author: windows-sdk-content
description: Skips over the specified number of user quota entries that are next in the enumeration sequence.
old-location: fs\ienumdiskquotausers_skip.htm
tech.root: FileIO
ms.assetid: b37462aa-cd1c-4986-ad23-f9523c962d19
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IEnumDiskQuotaUsers interface [Files],Skip method, IEnumDiskQuotaUsers.Skip, IEnumDiskQuotaUsers::Skip, Skip, Skip method [Files], Skip method [Files],IEnumDiskQuotaUsers interface, _win32_ienumdiskquotausers_skip, base.ienumdiskquotausers_skip, dskquota/IEnumDiskQuotaUsers::Skip, fs.ienumdiskquotausers_skip
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IEnumDiskQuotaUsers.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumDiskQuotaUsers::Skip


## -description


Skips over the specified number of user quota entries that are next in the enumeration 
    sequence.


## -parameters




### -param cUsers [in]

The number of elements to be skipped.


## -returns



The return value is <b>S_OK</b> if the number of elements skipped is 
       <i>cUsers</i>; otherwise, the return value is <b>S_FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/f5916b17-66ed-46d4-87f1-5ee2ef57c1a1">IEnumDiskQuotaUsers</a>
 

 

