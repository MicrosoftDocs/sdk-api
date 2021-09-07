---
UID: NN:dskquota.IDiskQuotaEvents
title: IDiskQuotaEvents (dskquota.h)
description: Receives quota-related event notifications.
helpviewer_keywords: ["IDiskQuotaEvents","IDiskQuotaEvents interface [Files]","IDiskQuotaEvents interface [Files]","described","_win32_idiskquotaevents","base.idiskquotaevents","dskquota/IDiskQuotaEvents","fs.idiskquotaevents"]
old-location: fs\idiskquotaevents.htm
tech.root: fs
ms.assetid: 4b5dcb1f-8edb-4fcb-94ea-2a627667071e
ms.date: 12/05/2018
ms.keywords: IDiskQuotaEvents, IDiskQuotaEvents interface [Files], IDiskQuotaEvents interface [Files],described, _win32_idiskquotaevents, base.idiskquotaevents, dskquota/IDiskQuotaEvents, fs.idiskquotaevents
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
 - IDiskQuotaEvents
 - dskquota/IDiskQuotaEvents
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
 - IDiskQuotaEvents
---

# IDiskQuotaEvents interface


## -description

A client must implement the 
<b>IDiskQuotaEvents</b> interface as an event sink that receives the quota-related event notifications. Its methods are called by the system whenever significant quota events have occurred. Currently, the only event supported is the asynchronous resolution of user account name information.

## -inheritance

The <b>IDiskQuotaEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDiskQuotaEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>
