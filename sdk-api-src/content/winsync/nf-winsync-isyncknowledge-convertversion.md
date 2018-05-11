---
UID: NF:winsync.ISyncKnowledge.ConvertVersion
title: ISyncKnowledge::ConvertVersion
author: windows-driver-content
description: Converts a version from another replica into one that is compatible with the replica that owns this knowledge.
old-location: winsync\isyncknowledge_convertversion.htm
old-project: winsync
ms.assetid: f41edaa3-7c4e-4b2c-9897-474b3e7bfb67
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ConvertVersion, ConvertVersion method [Windows Sync], ConvertVersion method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],ConvertVersion method, ISyncKnowledge.ConvertVersion, ISyncKnowledge::ConvertVersion, winsync.isyncknowledge_convertversion, winsync/ISyncKnowledge::ConvertVersion
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISyncKnowledge.ConvertVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncKnowledge::ConvertVersion


## -description


Converts a version from another replica into one that is compatible with the replica that owns this knowledge.


## -parameters




### -param pKnowledgeIn [in]

A knowledge that is valid for <i>pbCurrentOwnerId</i> and that contains <i>pVersionIn</i>.


### -param pbCurrentOwnerId [in]

The ID of the replica that owns <i>pVersionIn</i>.


### -param pVersionIn [in]

The version to convert.


### -param pbNewOwnerId [in]

Returns the ID of the replica that owns the converted version.


### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbNewOwnerId</i>. Returns the number of bytes required to retrieve the ID when <i>pbNewOwnerId</i> is too small, or returns the number of bytes written.


### -param pVersionOut [out]

Returns the version. This is converted to be valid for the replica that owns this knowledge.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbNewOwnerId</i> is too small. In this case, the required number of bytes is returned in <i>pcbIdSize</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/6a493a58-3dab-4032-90de-be9f903ae489">SYNC_VERSION Structure</a>
 

 

