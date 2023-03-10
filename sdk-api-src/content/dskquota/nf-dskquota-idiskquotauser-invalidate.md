---
UID: NF:dskquota.IDiskQuotaUser.Invalidate
title: IDiskQuotaUser::Invalidate (dskquota.h)
description: Invalidates the quota information stored in the quota user object.
helpviewer_keywords: ["IDiskQuotaUser interface [Files]","Invalidate method","IDiskQuotaUser.Invalidate","IDiskQuotaUser::Invalidate","Invalidate","Invalidate method [Files]","Invalidate method [Files]","IDiskQuotaUser interface","_win32_idiskquotauser_invalidate","base.idiskquotauser_invalidate","dskquota/IDiskQuotaUser::Invalidate","fs.idiskquotauser_invalidate"]
old-location: fs\idiskquotauser_invalidate.htm
tech.root: fs
ms.assetid: 23a51df4-0578-43fe-99cd-491f709accab
ms.date: 12/05/2018
ms.keywords: IDiskQuotaUser interface [Files],Invalidate method, IDiskQuotaUser.Invalidate, IDiskQuotaUser::Invalidate, Invalidate, Invalidate method [Files], Invalidate method [Files],IDiskQuotaUser interface, _win32_idiskquotauser_invalidate, base.idiskquotauser_invalidate, dskquota/IDiskQuotaUser::Invalidate, fs.idiskquotauser_invalidate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiskQuotaUser::Invalidate
 - dskquota/IDiskQuotaUser::Invalidate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IDiskQuotaUser.Invalidate
---

# IDiskQuotaUser::Invalidate


## -description

Invalidates the quota information stored in the quota user object. The next time information is requested, it is refreshed from disk.



## -returns

This method returns <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a>
