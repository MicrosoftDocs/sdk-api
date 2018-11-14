---
UID: NF:fsrmreports.IFsrmFileManagementJob.CreatePropertyCondition
title: IFsrmFileManagementJob::CreatePropertyCondition
author: windows-sdk-content
description: Creates a new property condition and adds it to the collection of property conditions.
old-location: fsrm\ifsrmfilemanagementjob_createpropertycondition.htm
tech.root: Fsrm
ms.assetid: 1b264e9c-4ba0-4de2-acdc-94338519c5af
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreatePropertyCondition, CreatePropertyCondition method [File Server Resource Manager], CreatePropertyCondition method [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],CreatePropertyCondition method, IFsrmFileManagementJob.CreatePropertyCondition, IFsrmFileManagementJob::CreatePropertyCondition, fs.ifsrmfilemanagementjob_createpropertycondition, fsrm.ifsrmfilemanagementjob_createpropertycondition, fsrmreports/IFsrmFileManagementJob::CreatePropertyCondition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: fsrmreports.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileManagementJob.CreatePropertyCondition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- fsrmreports.h
: 
- IFsrmFileManagementJob.CreatePropertyCondition
: 
---

# IFsrmFileManagementJob::CreatePropertyCondition


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

Creates a new property condition and adds it to the collection of property conditions.


## -parameters




### -param name [in]

The name of the property definition that the condition applies to. To enumerate the defined property 
      definitions, call the 
      <a href="https://msdn.microsoft.com/c97cb2f1-6e03-444e-a15e-faa85f7a7915">IFsrmClassificationManager::EnumPropertyDefinitions</a> 
      method.


### -param propertyCondition

TBD




#### - pPropertyCondition [out]

An <a href="https://msdn.microsoft.com/5c50b86b-f166-459e-92ce-63faa374c407">IFsrmPropertyCondition</a> interface that you 
      use to define the newly created property condition.


## -returns



The method returns the following return values.




## -remarks



To enumerate the collection of property conditions associated with the job, access the 
    <a href="https://msdn.microsoft.com/49435c4b-211e-4aae-a6b3-ad40de811526">PropertyConditions</a> 
    property.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

