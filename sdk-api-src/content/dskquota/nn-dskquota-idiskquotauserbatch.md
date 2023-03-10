---
UID: NN:dskquota.IDiskQuotaUserBatch
title: IDiskQuotaUserBatch (dskquota.h)
description: Adds multiple quota user objects to a container that is then submitted for update in a single call.
helpviewer_keywords: ["IDiskQuotaUserBatch","IDiskQuotaUserBatch interface [Files]","IDiskQuotaUserBatch interface [Files]","described","_win32_idiskquotauserbatch","base.idiskquotauserbatch","dskquota/IDiskQuotaUserBatch","fs.idiskquotauserbatch"]
old-location: fs\idiskquotauserbatch.htm
tech.root: fs
ms.assetid: 6cb3da5d-8e4c-45de-b9cf-0f6abf3f1932
ms.date: 12/05/2018
ms.keywords: IDiskQuotaUserBatch, IDiskQuotaUserBatch interface [Files], IDiskQuotaUserBatch interface [Files],described, _win32_idiskquotauserbatch, base.idiskquotauserbatch, dskquota/IDiskQuotaUserBatch, fs.idiskquotauserbatch
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
 - IDiskQuotaUserBatch
 - dskquota/IDiskQuotaUserBatch
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
 - IDiskQuotaUserBatch
---

# IDiskQuotaUserBatch interface


## -description

Adds multiple quota user objects to a container that is then submitted for update in a single call. This reduces the number of calls to the underlying file system, improving update efficiency when a large number of user objects must be updated. This interface is instantiated by using the 
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-createuserbatch">IDiskQuotaControl::CreateUserBatch</a> method.

## -inheritance

The <b>IDiskQuotaUserBatch</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDiskQuotaUserBatch</b> also has these types of members:

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>
