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
 

 

