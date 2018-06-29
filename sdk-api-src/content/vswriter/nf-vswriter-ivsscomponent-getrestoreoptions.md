---
UID: NF:vswriter.IVssComponent.GetRestoreOptions
title: IVssComponent::GetRestoreOptions
author: windows-sdk-content
description: The GetRestoreOptions method gets the restore options specified to the current writer by a requester using IVssBackupComponents::SetRestoreOptions.
old-location: base\ivsscomponent_getrestoreoptions.htm
old-project: VSS
ms.assetid: 818fd713-1b41-4abd-aca4-c74383fa3594
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetRestoreOptions, GetRestoreOptions method [VSS], GetRestoreOptions method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetRestoreOptions method, IVssComponent.GetRestoreOptions, IVssComponent::GetRestoreOptions, _win32_ivsscomponent_getrestoreoptions, base.ivsscomponent_getrestoreoptions, vswriter/IVssComponent::GetRestoreOptions
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
 - IVssComponent.GetRestoreOptions
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponent::GetRestoreOptions


## -description


The 
<b>GetRestoreOptions</b> method gets the restore options specified to the current writer by a requester using 
<a href="https://msdn.microsoft.com/4a872594-dcd8-463d-9f6b-6bc40c17df38">IVssBackupComponents::SetRestoreOptions</a>.

Either a writer or a requester can call this method.


## -parameters




### -param pbstrRestoreOptions [out]

String containing the restore options of the writer.


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
No restore options have been specified.

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



The caller should free the memory held by the <i>pbstrRestoreOptions</i> parameter by calling <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a>.

If no restore options have been set, S_FALSE is returned.




## -see-also




<a href="https://msdn.microsoft.com/4a872594-dcd8-463d-9f6b-6bc40c17df38">IVssBackupComponents::SetRestoreOptions</a>



<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/54182058-5dbb-4eda-959a-fa1921a27302">IVssComponent::GetBackupOptions</a>
 

 

