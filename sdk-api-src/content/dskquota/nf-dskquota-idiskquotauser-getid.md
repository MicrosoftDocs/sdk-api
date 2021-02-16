---
UID: NF:dskquota.IDiskQuotaUser.GetID
title: IDiskQuotaUser::GetID (dskquota.h)
description: Retrieves a unique identifier (ID) number for the DiskQuotaUser object.
helpviewer_keywords: ["GetID","GetID method [Files]","GetID method [Files]","IDiskQuotaUser interface","IDiskQuotaUser interface [Files]","GetID method","IDiskQuotaUser.GetID","IDiskQuotaUser::GetID","_win32_idiskquotauser_getid","base.idiskquotauser_getid","dskquota/IDiskQuotaUser::GetID","fs.idiskquotauser_getid"]
old-location: fs\idiskquotauser_getid.htm
tech.root: fs
ms.assetid: 04f84fd1-9ce4-4daa-91b3-24508f326f84
ms.date: 12/05/2018
ms.keywords: GetID, GetID method [Files], GetID method [Files],IDiskQuotaUser interface, IDiskQuotaUser interface [Files],GetID method, IDiskQuotaUser.GetID, IDiskQuotaUser::GetID, _win32_idiskquotauser_getid, base.idiskquotauser_getid, dskquota/IDiskQuotaUser::GetID, fs.idiskquotauser_getid
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
 - IDiskQuotaUser::GetID
 - dskquota/IDiskQuotaUser::GetID
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
 - IDiskQuotaUser.GetID
---

# IDiskQuotaUser::GetID


## -description

Retrieves a unique identifier (ID) number for the <a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">DiskQuotaUser</a> object. This ID is unique only within the process. It can be used to identify a user object in a set of user objects if the programming language you are using does not support pointers.

## -parameters

### -param pulID [out]

The name strings associated with the disk quota user.

## -returns

This method returns <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a>