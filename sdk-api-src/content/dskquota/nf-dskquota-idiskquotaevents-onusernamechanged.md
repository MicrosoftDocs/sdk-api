---
UID: NF:dskquota.IDiskQuotaEvents.OnUserNameChanged
title: IDiskQuotaEvents::OnUserNameChanged (dskquota.h)
description: Notifies the client's connection sink whenever a user's SID has been asynchronously resolved.
helpviewer_keywords: ["IDiskQuotaEvents interface [Files]","OnUserNameChanged method","IDiskQuotaEvents.OnUserNameChanged","IDiskQuotaEvents::OnUserNameChanged","OnUserNameChanged","OnUserNameChanged method [Files]","OnUserNameChanged method [Files]","IDiskQuotaEvents interface","_win32_idiskquotaevents_onusernamechanged","base.idiskquotaevents_onusernamechanged","dskquota/IDiskQuotaEvents::OnUserNameChanged","fs.idiskquotaevents_onusernamechanged"]
old-location: fs\idiskquotaevents_onusernamechanged.htm
tech.root: fs
ms.assetid: d01cb679-03e2-4b76-b068-f64e576709fb
ms.date: 12/05/2018
ms.keywords: IDiskQuotaEvents interface [Files],OnUserNameChanged method, IDiskQuotaEvents.OnUserNameChanged, IDiskQuotaEvents::OnUserNameChanged, OnUserNameChanged, OnUserNameChanged method [Files], OnUserNameChanged method [Files],IDiskQuotaEvents interface, _win32_idiskquotaevents_onusernamechanged, base.idiskquotaevents_onusernamechanged, dskquota/IDiskQuotaEvents::OnUserNameChanged, fs.idiskquotaevents_onusernamechanged
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
 - IDiskQuotaEvents::OnUserNameChanged
 - dskquota/IDiskQuotaEvents::OnUserNameChanged
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
 - IDiskQuotaEvents.OnUserNameChanged
---

# IDiskQuotaEvents::OnUserNameChanged


## -description

Notifies the client's connection sink whenever a user's SID has been asynchronously resolved. If 
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getaccountstatus">IDiskQuotaUser::GetAccountStatus</a> returns DISKQUOTA_USER_ACCOUNT_RESOLVED, the user's account container name, logon name, and display name strings are available in the quota user object.

## -parameters

### -param pUser [in]

A pointer to the 
<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotauser">IDiskQuotaUser</a> interface for the quota user object. Do not  call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on this pointer. The <b>DiskQuotaControl</b> object controls the lifetime of the user object.

## -returns

The return value is ignored.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotaevents">IDiskQuotaEvents</a>