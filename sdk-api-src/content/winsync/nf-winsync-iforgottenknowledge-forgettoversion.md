---
UID: NF:winsync.IForgottenKnowledge.ForgetToVersion
title: IForgottenKnowledge::ForgetToVersion
author: windows-sdk-content
description: Updates the forgotten knowledge to reflect that all versions that are less than or equal to the specified version might have been forgotten, and that corresponding tombstones might have been deleted.
old-location: winsync\iforgottenknowledge_forgettoversion.htm
tech.root: winsync
ms.assetid: 63ea1fdc-5200-40d4-a42a-dcda0318f602
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ForgetToVersion, ForgetToVersion method [Windows Sync], ForgetToVersion method [Windows Sync],IForgottenKnowledge interface, IForgottenKnowledge interface [Windows Sync],ForgetToVersion method, IForgottenKnowledge.ForgetToVersion, IForgottenKnowledge::ForgetToVersion, winsync.iforgottenknowledge_forgettoversion, winsync/IForgottenKnowledge::ForgetToVersion
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
 - IForgottenKnowledge.ForgetToVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IForgottenKnowledge::ForgetToVersion


## -description


Updates the forgotten knowledge to reflect that all versions that are less than or equal to the specified version might have been forgotten, and that corresponding tombstones might have been deleted.


## -parameters




### -param pKnowledge [in]

The current knowledge of the replica that owns this forgotten knowledge object.


### -param pVersion [in]

The version of the tombstone that has been cleaned up.


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
</table>
 




## -remarks



When a replica cleans up the tombstone for an item, its associated provider must call this method and specify the version of the tombstone that was removed.




## -see-also




<a href="https://msdn.microsoft.com/93185921-8f41-4222-86d8-602d197c4b33">IForgottenKnowledge Interface</a>



<a href="https://msdn.microsoft.com/6a493a58-3dab-4032-90de-be9f903ae489">SYNC_VERSION Structure</a>
 

 

