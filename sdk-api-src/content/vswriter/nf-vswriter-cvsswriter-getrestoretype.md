---
UID: NF:vswriter.CVssWriter.GetRestoreType
title: CVssWriter::GetRestoreType
author: windows-sdk-content
description: The GetRestoreType method returns the type of restore a writer is participating in.
old-location: base\cvsswriter_getrestoretype.htm
tech.root: vss
ms.assetid: 438298ee-ab8b-4604-9d43-5acefd7cabd5
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CVssWriter interface [VSS],GetRestoreType method, CVssWriter.GetRestoreType, CVssWriter::GetRestoreType, GetRestoreType, GetRestoreType method [VSS], GetRestoreType method [VSS],CVssWriter interface, _win32_cvsswriter_getrestoretype, base.cvsswriter_getrestoretype, vswriter/CVssWriter::GetRestoreType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - CVssWriter.GetRestoreType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CVssWriter::GetRestoreType


## -description


The 
<b>GetRestoreType</b> method returns the type of restore a writer is participating in.

<b>GetRestoreType</b> is a protected method implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class.


## -parameters






## -returns



This method returns the type of restore operation a writer is participating in, in terms of values of the 
<a href="https://msdn.microsoft.com/4649aee5-da45-4602-a768-eff228a8d726">VSS_RESTORE_TYPE</a> enumeration.

If 
<b>GetRestoreType</b> is called during a backup operation, the return value is undefined.




## -remarks



This method should be called only during restore operations.

The default restore type is VSS_RTYPE_UNDEFINED. However, writers should treat this restore type as if it were VSS_RTYPE_BY_COPY.

A requester can set the restore type by calling the 
<a href="https://msdn.microsoft.com/bc85e93f-1034-41cc-bf69-025aa86a56fd">IVssBackupComponents::SetRestoreState</a> method.

A requester can call <a href="https://msdn.microsoft.com/bc85e93f-1034-41cc-bf69-025aa86a56fd">IVssBackupComponents::SetRestoreState</a> anytime prior to its generation of a 
<a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">PreRestore</a> event with the 
<b>IVssBackupComponents::PreRestore</b> method. Therefore, to obtain the correct restore type, a writer should not call 
<b>GetRestoreType</b> prior to handling the 
<b>PreRestore</b> event in 
<a href="https://msdn.microsoft.com/5f4a6168-4102-4790-81d6-d195a440471f">CVssWriter::OnPreRestore</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/5f4a6168-4102-4790-81d6-d195a440471f">CVssWriter::OnPreRestore</a>



<a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">IVssBackupComponents::PreRestore</a>



<a href="https://msdn.microsoft.com/bc85e93f-1034-41cc-bf69-025aa86a56fd">IVssBackupComponents::SetRestoreState</a>



<a href="https://msdn.microsoft.com/4649aee5-da45-4602-a768-eff228a8d726">VSS_RESTORE_TYPE</a>
 

 

