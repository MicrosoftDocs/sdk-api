---
UID: NF:vswriter.IVssComponent.GetPreviousBackupStamp
title: IVssComponent::GetPreviousBackupStamp
author: windows-sdk-content
description: The GetPreviousBackupStamp method returns a previous backup stamp loaded by a requester in the Backup Components Document. The value is used by a writer when deciding if files should participate in differential or incremental backup operation.
old-location: base\ivsscomponent_getpreviousbackupstamp.htm
old-project: VSS
ms.assetid: 91778854-52af-4e1e-943b-89c786963291
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetPreviousBackupStamp, GetPreviousBackupStamp method [VSS], GetPreviousBackupStamp method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetPreviousBackupStamp method, IVssComponent.GetPreviousBackupStamp, IVssComponent::GetPreviousBackupStamp, _win32_ivsscomponent_getpreviousbackupstamp, base.ivsscomponent_getpreviousbackupstamp, vswriter/IVssComponent::GetPreviousBackupStamp
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssComponent.GetPreviousBackupStamp
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponent::GetPreviousBackupStamp


## -description


The 
<b>GetPreviousBackupStamp</b> method returns a previous backup stamp loaded by a requester in the Backup Components Document. The value is used by a writer when deciding if files should participate in differential or incremental backup operation.

Either a writer or a requester can call this method.


## -parameters




### -param pbstrBackupStamp [out]

Pointer to a string containing the time stamp of a previous backup so that a differential or incremental backup can be correctly implemented.


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
No previous backup time stamp has been set.

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



For more information about backup stamps, see <a href="https://msdn.microsoft.com/3cf5dd1f-dc58-42bc-925f-fee7d34053c5">Writer Role in Backing Up Complex Stores</a> and <a href="https://msdn.microsoft.com/00391a49-8c81-4518-88a2-741ad5ee4ac3">Requester Role in Backing Up Complex Stores</a>.

The caller should free the memory held by the <i>pbstrBackupStamp</i> parameter by calling <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>.

If there is no previous backup time stamp, 
<b>GetPreviousBackupStamp</b> returns S_FALSE.

The string returned refers to all files in the component and any nonselectable subcomponents it has.

The backup stamp retrieved by 
<b>GetPreviousBackupStamp</b> is set by a requester using 
<a href="https://msdn.microsoft.com/cc1c75bf-b281-4741-9273-f7264532860f">IVssBackupComponents::SetPreviousBackupStamp</a>.

Typically, the string used to set the value found by 
<b>GetPreviousBackupStamp</b> was retrieved from a stored Backup Components Document or was stored by the requester as part of its own internal records.




## -see-also




<a href="https://msdn.microsoft.com/cc1c75bf-b281-4741-9273-f7264532860f">IVssBackupComponents::SetPreviousBackupStamp</a>



<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>
 

 

