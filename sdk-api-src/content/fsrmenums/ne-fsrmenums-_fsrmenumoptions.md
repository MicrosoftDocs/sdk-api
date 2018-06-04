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

# _FsrmEnumOptions enumeration


## -description


Defines the options for enumerating collections of objects.


## -enum-fields




### -field FsrmEnumOptions_None

Use no options and enumerate objects synchronously.


### -field FsrmEnumOptions_Asynchronous

Reserved. Do not use.


### -field FsrmEnumOptions_CheckRecycleBin

Include items and paths that are in the system recycle bin when enumerating.


### -field FsrmEnumOptions_IncludeClusterNodes

Include objects on all nodes in a <a href="https://msdn.microsoft.com/47247d48-d401-41dc-9aae-128840eb6d3a">Windows cluster</a> 
      when enumerating report jobs 
      (<a href="https://msdn.microsoft.com/af66beb6-e82c-47e6-8658-da9702041053">IFsrmReportManager::EnumReportJobs</a>).


### -field FsrmEnumOptions_IncludeDeprecatedObjects

Include deprecated objects when enumerating.

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This enumeration value is not supported before Windows Server 2012.


## -remarks



The <b>FsrmEnumOptions_Asynchronous</b> option is not supported.




## -see-also




<a href="https://msdn.microsoft.com/eeda0802-e450-4a8b-a08c-135784540b17">IFsrmClassificationManager::EnumModuleDefinitions</a>



<a href="https://msdn.microsoft.com/c97cb2f1-6e03-444e-a15e-faa85f7a7915">IFsrmClassificationManager::EnumPropertyDefinitions</a>



<a href="https://msdn.microsoft.com/2f67527c-cde3-4907-9e61-4d9e18b18859">IFsrmClassificationManager::EnumRules</a>



<a href="https://msdn.microsoft.com/317eb6cf-7bcc-4042-a7b7-05efac84a0c2">IFsrmFileGroupManager::EnumFileGroups</a>



<a href="https://msdn.microsoft.com/4af6f794-d9d4-4e03-9cd5-a4d8769888ca">IFsrmFileManagementJobManager::EnumFileManagementJobs</a>



<a href="https://msdn.microsoft.com/c30377c8-d3a3-40fe-a42c-9b36d2a0b35e">IFsrmFileScreenManager::EnumFileScreenExceptions</a>



<a href="https://msdn.microsoft.com/5826d5c3-885a-4001-aa89-0bc1c03b9338">IFsrmFileScreenManager::EnumFileScreens</a>



<a href="https://msdn.microsoft.com/5bfb82f9-50a5-4266-956d-f99e2982a6a5">IFsrmFileScreenTemplateManager::EnumTemplates</a>



<a href="https://msdn.microsoft.com/6542bc4e-535f-4e6c-aaa8-ba6963490811">IFsrmQuotaManager::EnumAutoApplyQuotas</a>



<a href="https://msdn.microsoft.com/abe5e73b-459a-4e2a-9917-91d3c85a15bc">IFsrmQuotaManager::EnumEffectiveQuotas</a>



<a href="https://msdn.microsoft.com/9977a519-4a6d-4b35-b973-4ef086e13e92">IFsrmQuotaManager::EnumQuotas</a>



<a href="https://msdn.microsoft.com/8b366eae-5554-4c20-9ba9-c3a6e319712f">IFsrmQuotaManagerEx::IsAffectedByQuota</a>



<a href="https://msdn.microsoft.com/e5f5b94a-6b17-4379-9141-07ec70a830e9">IFsrmQuotaTemplateManager::EnumTemplates</a>



<a href="https://msdn.microsoft.com/af66beb6-e82c-47e6-8658-da9702041053">IFsrmReportManager::EnumReportJobs</a>
 

 

