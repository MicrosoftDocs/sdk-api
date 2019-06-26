---
UID: NF:dskquota.IEnumDiskQuotaUsers.Skip
title: IEnumDiskQuotaUsers::Skip (dskquota.h)
author: windows-sdk-content
description: Skips over the specified number of user quota entries that are next in the enumeration sequence.
old-location: fs\ienumdiskquotausers_skip.htm
tech.root: FileIO
ms.assetid: b37462aa-cd1c-4986-ad23-f9523c962d19
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumDiskQuotaUsers interface [Files],Skip method, IEnumDiskQuotaUsers.Skip, IEnumDiskQuotaUsers::Skip, Skip, Skip method [Files], Skip method [Files],IEnumDiskQuotaUsers interface, _win32_ienumdiskquotausers_skip, base.ienumdiskquotausers_skip, dskquota/IEnumDiskQuotaUsers::Skip, fs.ienumdiskquotausers_skip
ms.topic: method
f1_keywords: 
 - "dskquota/IEnumDiskQuotaUsers.Skip"
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
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nn-dskquota-ienumdiskquotausers">IEnumDiskQuotaUsers</a>
 

 

