---
UID: NE:vswriter.VSS_WRITERRESTORE_ENUM
title: VSS_WRITERRESTORE_ENUM (vswriter.h)
author: windows-sdk-content
description: Indicate to a requester the conditions under which it will handle events generated during a restore operation.
old-location: base\vss_writerrestore_enum.htm
tech.root: VSS
ms.assetid: a3e45d52-4d9a-4bdf-a8e5-622939be6f2c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VSS_WRE_ALWAYS, VSS_WRE_IF_REPLACE_FAILS, VSS_WRE_NEVER, VSS_WRE_UNDEFINED, VSS_WRITERRESTORE_ENUM, VSS_WRITERRESTORE_ENUM enumeration [VSS], _win32_vss_writerrestore_enum, base.vss_writerrestore_enum, enumeration [VSS], vswriter/VSS_WRE_ALWAYS, vswriter/VSS_WRE_IF_REPLACE_FAILS, vswriter/VSS_WRE_NEVER, vswriter/VSS_WRE_UNDEFINED, vswriter/VSS_WRITERRESTORE_ENUM
ms.topic: enum
req.header: vswriter.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsWriter.h
api_name:
 - VSS_WRITERRESTORE_ENUM
product: Windows
targetos: Windows
req.typenames: VSS_WRITERRESTORE_ENUM
req.redist: 
ms.custom: 19H1
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
 

 

