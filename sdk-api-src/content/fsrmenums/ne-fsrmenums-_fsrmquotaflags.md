---
UID: NE:fsrmenums._FsrmQuotaFlags
title: "_FsrmQuotaFlags"
author: windows-sdk-content
description: Defines the options for failing IO operations that violate a quota, enabling or disabling quota tracking, and providing the status of the quota scan operation.
old-location: fsrm\fsrmquotaflags.htm
old-project: fsrm
ms.assetid: 254a26c7-a859-4b23-a3e2-9d261c848eef
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: FsrmQuotaFlags, FsrmQuotaFlags enumeration [File Server Resource Manager], FsrmQuotaFlags_Disable, FsrmQuotaFlags_Enforce, FsrmQuotaFlags_StatusIncomplete, FsrmQuotaFlags_StatusRebuilding, _FsrmQuotaFlags, fs.fsrmquotaflags, fsrm.fsrmquotaflags, fsrmenums/FsrmQuotaFlags, fsrmenums/FsrmQuotaFlags_Disable, fsrmenums/FsrmQuotaFlags_Enforce, fsrmenums/FsrmQuotaFlags_StatusIncomplete, fsrmenums/FsrmQuotaFlags_StatusRebuilding
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmEnums.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FsrmQuotaFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmQuotaFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# _FsrmQuotaFlags enumeration


## -description


Defines the options for failing IO operations that violate a quota, enabling or disabling quota 
    tracking, and providing the status of the quota scan operation.


## -enum-fields




### -field FsrmQuotaFlags_Enforce

If this flag is set, the server will fail an IO operation that causes the disk space usage to exceed the 
     quota limit. If this flag is not set, the server will not fail violating IO operations but will still run any 
     action associated with the quota thresholds.


### -field FsrmQuotaFlags_Disable

The server will not track quota data for the quota and will not run any action associated with quota 
     thresholds.


### -field FsrmQuotaFlags_StatusIncomplete

The quota is defined on the server but the rebuilding procedure (see 
     <a href="https://msdn.microsoft.com/1581f4c7-a912-4214-9ad9-181ad5ebba7e">IFsrmQuotaManager::Scan</a>) did not start or the scan 
     failed.


### -field FsrmQuotaFlags_StatusRebuilding

The quota is in the process of rebuilding its data from the disk.


## -remarks



You can set the <b>FsrmQuotaFlags_Enforce</b> and 
    <b>FsrmQuotaFlags_Disable</b> flags when calling the 
    <a href="https://msdn.microsoft.com/af856281-8161-4165-bf24-0c160f7394d2">IFsrmQuotaBase::put_QuotaFlags</a> method. The 
    <b>IFsrmQuotaBase::get_QuotaFlags</b> method can return 
    these flags in addition to the <b>FsrmQuotaFlags_StatusIncomplete</b> and 
    <b>FsrmQuotaFlags_StatusRebuilding</b> flags.




## -see-also




<a href="https://msdn.microsoft.com/af856281-8161-4165-bf24-0c160f7394d2">IFsrmQuotaBase::QuotaFlags</a>
 

 

