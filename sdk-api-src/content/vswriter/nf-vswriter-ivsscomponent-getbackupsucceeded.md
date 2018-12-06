---
UID: NF:vswriter.IVssComponent.GetBackupSucceeded
title: IVssComponent::GetBackupSucceeded
author: windows-sdk-content
description: The GetBackupSucceeded method returns the status of a complete attempt at backing up all the files of a selected component or component set as a VSS_FILE_RESTORE_STATUS enumeration.
old-location: base\ivsscomponent_getbackupsucceeded.htm
tech.root: vss
ms.assetid: 9b2dce08-a4ab-4e55-aeef-819f71ddf9d2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetBackupSucceeded, GetBackupSucceeded method [VSS], GetBackupSucceeded method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetBackupSucceeded method, IVssComponent.GetBackupSucceeded, IVssComponent::GetBackupSucceeded, _win32_ivsscomponent_getbackupsucceeded, base.ivsscomponent_getbackupsucceeded, vswriter/IVssComponent::GetBackupSucceeded
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
 - IVssComponent.GetBackupSucceeded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssComponent::GetBackupSucceeded


## -description


The 
<b>GetBackupSucceeded</b> method returns the status of a complete attempt at backing up all the files of a selected component or component set as a 
<a href="https://msdn.microsoft.com/e1754fad-8da1-4a3e-a70a-ada37dde1c5d">VSS_FILE_RESTORE_STATUS</a> enumeration. (See 
<a href="https://msdn.microsoft.com/e8920cca-d944-437f-bf6a-7ce8d518746a">Working with Selectability and Logical Paths</a> for information on selecting components.)

Either a writer or a requester can call this method.


## -parameters




### -param pbSucceeded [out]

The address of a caller-allocated variable that receives <b>true</b> if the backup was successful, or <b>false</b> otherwise.


## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully returned the attribute value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The backup success state is undefined because the method was called prior to a 
<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> event.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
<a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

</td>
</tr>
</table>
 




## -remarks



This method should not be called prior to a 
<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> event, and is designed for use in an implementation of the event handler 
<a href="https://msdn.microsoft.com/77d0621d-81bd-4d53-8e5d-f5d3bfd86013">CVssWriter::OnBackupComplete</a>.




## -see-also




<a href="https://msdn.microsoft.com/77d0621d-81bd-4d53-8e5d-f5d3bfd86013">CVssWriter::OnBackupComplete</a>



<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>
 

 

