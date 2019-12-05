---
UID: NF:dskquota.IEnumDiskQuotaUsers.Next
title: IEnumDiskQuotaUsers::Next (dskquota.h)
description: Retrieves the specified number of user quota entries that are next in the enumeration sequence.
old-location: fs\ienumdiskquotausers_next.htm
tech.root: FileIO
ms.assetid: 498e7c21-b18a-4d43-bbe6-9f20c2e26221
ms.date: 12/05/2018
ms.keywords: IEnumDiskQuotaUsers interface [Files],Next method, IEnumDiskQuotaUsers.Next, IEnumDiskQuotaUsers::Next, Next, Next method [Files], Next method [Files],IEnumDiskQuotaUsers interface, _win32_ienumdiskquotausers_next, base.ienumdiskquotausers_next, dskquota/IEnumDiskQuotaUsers::Next, fs.ienumdiskquotausers_next
ms.topic: method
f1_keywords:
- dskquota/IEnumDiskQuotaUsers.Next
dev_langs:
- c++
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
- IEnumDiskQuotaUsers.Next
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumDiskQuotaUsers::Next


## -description


Retrieves the specified number of user quota entries that are next in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.


## -parameters




### -param cUsers [in]

The number of elements being requested.


### -param rgUsers [out]

An array of size <i>cUsers</i> or larger.


### -param pcUsersFetched [in, out]

On input, the number of elements in <i>rgUsers</i>, on input. On output, the number of elements actually retrieved. The caller can pass in <b>NULL</b> if <i>cUsers</i> is one and the number of elements retrieved is of no interest.


## -returns



The return value is <b>S_OK</b> if the number of elements supplied is <i>cUsers</i>; otherwise, the return value is <b>S_FALSE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nn-dskquota-ienumdiskquotausers">IEnumDiskQuotaUsers</a>
 

 

