---
UID: NL:vsbackup.IVssWriterComponentsExt
title: IVssWriterComponentsExt (vsbackup.h)
author: windows-sdk-content
description: The IVssWriterComponentsExt interface is a C++ (not COM) interface used by requesters to access and modify the components of a writer involved in a backup.
old-location: base\ivsswritercomponentsext.htm
tech.root: VSS
ms.assetid: 29772c1f-1cc4-4ee7-8e1d-f1a6cbebf470
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVssWriterComponentsExt, IVssWriterComponentsExt interface [VSS], IVssWriterComponentsExt interface [VSS],described, _win32_ivsswritercomponentsext, base.ivsswritercomponentsext, vsbackup/IVssWriterComponentsExt
ms.topic: class
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
 - IVssWriterComponentsExt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssWriterComponentsExt class


## -description


The 
<b>IVssWriterComponentsExt</b> interface is a C++ (not COM) interface used by requesters to access and modify the components of a writer involved in a backup.

<b>IVssWriterComponentsExt</b> is returned by 
<a href="https://msdn.microsoft.com/b99e7e41-1c88-462c-b6d8-734f7a6e24d4">IVssBackupComponents::GetWriterComponents</a> and inherits from 
<a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a> and <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>.
<div class="alert"><b>Note</b>  During the restore phase, the requester should call <a href="https://msdn.microsoft.com/ee816d83-31f3-47ff-b581-cc4dcd878f22">IVssWriterComponentsExt::GetComponent</a> or <a href="https://msdn.microsoft.com/ec89438f-4811-42f7-bda0-6df6d1b98f18">IVssWriterComponentsExt::GetComponentCount</a> only after the call to <a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">IVssBackupComponents::PreRestore</a> has returned, to allow time for the writer to update the Backup Components Document. One example of such an update would be to change the restore target.</div><div> </div>Life cycle management of 
<b>IVssWriterComponentsExt</b> is handled through the inherited <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> methods. Specifically, an application is responsible for calling <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> to release resources held by an 
<b>IVssWriterComponentsExt</b> object.

<b>IVssWriterComponentsExt</b> does not define any methods.

