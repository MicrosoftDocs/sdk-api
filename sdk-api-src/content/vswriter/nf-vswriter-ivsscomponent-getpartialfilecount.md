---
UID: NF:vswriter.IVssComponent.GetPartialFileCount
title: IVssComponent::GetPartialFileCount
author: windows-sdk-content
description: The GetPartialFileCount method returns the number of partial files associated with a component.
old-location: base\ivsscomponent_getpartialfilecount.htm
tech.root: vss
ms.assetid: 7be84c00-49c4-4c44-9c12-7994247726a5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPartialFileCount, GetPartialFileCount method [VSS], GetPartialFileCount method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetPartialFileCount method, IVssComponent.GetPartialFileCount, IVssComponent::GetPartialFileCount, _win32_ivsscomponent_getpartialfilecount, base.ivsscomponent_getpartialfilecount, vswriter/IVssComponent::GetPartialFileCount
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
 - IVssComponent.GetPartialFileCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssComponent::GetPartialFileCount


## -description


The 
<b>GetPartialFileCount</b> method returns the number of partial files associated with a component.


## -parameters




### -param pcPartialFiles [out]

The address of a caller-allocated variable that receives the number of partial files.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/170f9ea0-4846-49d4-ab06-eb1ce580e827">IVssBackupComponents::SetRangesFilePath</a>



<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/318dc1ee-e63f-4e79-96b9-8a8bd83facd3">IVssComponent::AddPartialFile</a>



<a href="https://msdn.microsoft.com/ed589ae8-2abb-4c3b-9695-12649fc89818">IVssComponent::GetPartialFile</a>
 

 

