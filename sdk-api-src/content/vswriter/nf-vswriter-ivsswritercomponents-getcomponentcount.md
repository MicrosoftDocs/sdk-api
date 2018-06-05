---
UID: NF:vswriter.IVssWriterComponents.GetComponentCount
title: IVssWriterComponents::GetComponentCount
author: windows-sdk-content
description: The GetComponentCount method returns the number of a given writer's components explicitly stored in the Backup Components Document.
old-location: base\ivsswritercomponents_getcomponentcount.htm
old-project: VSS
ms.assetid: ec89438f-4811-42f7-bda0-6df6d1b98f18
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetComponentCount, GetComponentCount method [VSS], GetComponentCount method [VSS],IVssWriterComponents interface, IVssWriterComponents interface [VSS],GetComponentCount method, IVssWriterComponents.GetComponentCount, IVssWriterComponents::GetComponentCount, _win32_ivsswritercomponents_getcomponentcount, base.ivsswritercomponents_getcomponentcount, vswriter/IVssWriterComponents::GetComponentCount
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssWriterComponents.GetComponentCount
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssWriterComponents::GetComponentCount


## -description


The 
<b>GetComponentCount</b> method returns the number of a given writer's components explicitly stored in the Backup Components Document.


## -parameters




### -param pcComponents [out]

Pointer to the number of a writer's components stored in the Backup Components Document.


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
Successfully returned the component.

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




<a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a>
 

 

