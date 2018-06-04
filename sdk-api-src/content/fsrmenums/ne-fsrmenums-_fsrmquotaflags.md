---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

