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

# VSS_WRITERRESTORE_ENUM enumeration


## -description


The <b>VSS_WRITERRESTORE_ENUM</b> numeration is used by 
    a writer to indicate to a requester the conditions under which it will handle events generated during a 
    restore operation.


## -enum-fields




### -field VSS_WRE_UNDEFINED

It is not known whether the writer will perform special operations during the restore operation. 
      

This state indicates a writer error.


### -field VSS_WRE_NEVER

The writer does not require restore events.


### -field VSS_WRE_IF_REPLACE_FAILS

Indicates that the writer always expects to handle a 
      <a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">PreRestore</a> 
      (<a href="https://msdn.microsoft.com/5f4a6168-4102-4790-81d6-d195a440471f">CvssWriter::OnPreRestore</a>) event, but expects 
      to handle a <a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a> event 
      (<a href="https://msdn.microsoft.com/ad07753c-1592-4fc8-9899-a73e798c158c">CvssWriter::OnPostRestore</a>) only if a restore 
      fails when implementing either a <b>VSS_RME_RESTORE_IF_NOT_THERE</b> or 
      <b>VSS_RME_RESTORE_IF_CAN_REPLACE</b> restore method 
      (<a href="https://msdn.microsoft.com/4c6be981-4271-4040-8f6e-725616355062">VSS_RESTOREMETHOD_ENUM</a>).


### -field VSS_WRE_ALWAYS

The writer always performs special operations during the restore operation.


## -remarks



A writer passes a value of 
    <b>VSS_WRITERRESTORE_ENUM</b> to 
    <a href="https://msdn.microsoft.com/0e04df40-49e4-4f23-b4d5-d6b602162935">IVssCreateWriterMetadata::SetRestoreMethod</a> 
    to indicate through its metadata how it interacts with requesters during a restore operation.

A requester retrieves information about a writer's participation by calling 
    <a href="https://msdn.microsoft.com/c93f841f-057c-4aee-b8f2-263395e84c7b">IVssExamineWriterMetadata::GetRestoreMethod</a>.




## -see-also




<a href="https://msdn.microsoft.com/0e04df40-49e4-4f23-b4d5-d6b602162935">IVssCreateWriterMetadata::SetRestoreMethod</a>



<a href="https://msdn.microsoft.com/c93f841f-057c-4aee-b8f2-263395e84c7b">IVssExamineWriterMetadata::GetRestoreMethod</a>



<a href="https://msdn.microsoft.com/4c6be981-4271-4040-8f6e-725616355062">VSS_RESTOREMETHOD_ENUM</a>
 

 

