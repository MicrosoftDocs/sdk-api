---
UID: NE:fsrmenums._FsrmQuotaFlags
title: FsrmQuotaFlags (fsrmenums.h)
description: Defines the options for failing IO operations that violate a quota, enabling or disabling quota tracking, and providing the status of the quota scan operation.
helpviewer_keywords: ["FsrmQuotaFlags","FsrmQuotaFlags enumeration [File Server Resource Manager]","FsrmQuotaFlags_Disable","FsrmQuotaFlags_Enforce","FsrmQuotaFlags_StatusIncomplete","FsrmQuotaFlags_StatusRebuilding","fs.fsrmquotaflags","fsrm.fsrmquotaflags","fsrmenums/FsrmQuotaFlags","fsrmenums/FsrmQuotaFlags_Disable","fsrmenums/FsrmQuotaFlags_Enforce","fsrmenums/FsrmQuotaFlags_StatusIncomplete","fsrmenums/FsrmQuotaFlags_StatusRebuilding"]
old-location: fsrm\fsrmquotaflags.htm
tech.root: fsrm
ms.assetid: 254a26c7-a859-4b23-a3e2-9d261c848eef
ms.date: 12/05/2018
ms.keywords: FsrmQuotaFlags, FsrmQuotaFlags enumeration [File Server Resource Manager], FsrmQuotaFlags_Disable, FsrmQuotaFlags_Enforce, FsrmQuotaFlags_StatusIncomplete, FsrmQuotaFlags_StatusRebuilding, fs.fsrmquotaflags, fsrm.fsrmquotaflags, fsrmenums/FsrmQuotaFlags, fsrmenums/FsrmQuotaFlags_Disable, fsrmenums/FsrmQuotaFlags_Enforce, fsrmenums/FsrmQuotaFlags_StatusIncomplete, fsrmenums/FsrmQuotaFlags_StatusRebuilding
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FsrmQuotaFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmQuotaFlags
 - fsrmenums/_FsrmQuotaFlags
 - FsrmQuotaFlags
 - fsrmenums/FsrmQuotaFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmQuotaFlags
---

# FsrmQuotaFlags enumeration


## -description

Defines the options for failing IO operations that violate a quota, enabling or disabling quota 
    tracking, and providing the status of the quota scan operation.

## -enum-fields

### -field FsrmQuotaFlags_Enforce:0x100

If this flag is set, the server will fail an IO operation that causes the disk space usage to exceed the 
     quota limit. If this flag is not set, the server will not fail violating IO operations but will still run any 
     action associated with the quota thresholds.

### -field FsrmQuotaFlags_Disable:0x200

The server will not track quota data for the quota and will not run any action associated with quota 
     thresholds.

### -field FsrmQuotaFlags_StatusIncomplete:0x10000

The quota is defined on the server but the rebuilding procedure (see 
     <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-scan">IFsrmQuotaManager::Scan</a>) did not start or the scan 
     failed.

### -field FsrmQuotaFlags_StatusRebuilding:0x20000

The quota is in the process of rebuilding its data from the disk.

## -remarks

You can set the <b>FsrmQuotaFlags_Enforce</b> and 
    <b>FsrmQuotaFlags_Disable</b> flags when calling the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-get_quotaflags">IFsrmQuotaBase::put_QuotaFlags</a> method. The 
    <b>IFsrmQuotaBase::get_QuotaFlags</b> method can return 
    these flags in addition to the <b>FsrmQuotaFlags_StatusIncomplete</b> and 
    <b>FsrmQuotaFlags_StatusRebuilding</b> flags.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-get_quotaflags">IFsrmQuotaBase::QuotaFlags</a>
