---
UID: NF:winsync.ISyncKnowledge.GetVersion
title: ISyncKnowledge::GetVersion
author: windows-sdk-content
description: Gets the version of this knowledge structure.
old-location: winsync\isyncknowledge_getversion.htm
tech.root: winsync
ms.assetid: b54114f1-aa54-493d-b449-0b9161004ffa
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetVersion, GetVersion method [Windows Sync], GetVersion method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],GetVersion method, ISyncKnowledge.GetVersion, ISyncKnowledge::GetVersion, winsync.isyncknowledge_getversion, winsync/ISyncKnowledge::GetVersion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncKnowledge.GetVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- winsync.h
: 
- ISyncKnowledge.GetVersion
: 
---

# ISyncKnowledge::GetVersion


## -description


Gets the version of this knowledge structure.


## -parameters




### -param pdwVersion [out]

Returns the version of this knowledge structure. is one of the values in the <a href="https://msdn.microsoft.com/840a1f5e-56f7-4774-a154-0dab66c3d407">SYNC_SERIALIZATION_VERSION</a> enumeration.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>
 




## -remarks



This value is the version of the knowledge structure itself. When the internal knowledge structure is changed, the version that this method returns will also be changed.




## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/840a1f5e-56f7-4774-a154-0dab66c3d407">SYNC_SERIALIZATION_VERSION Enumeration</a>
 

 

