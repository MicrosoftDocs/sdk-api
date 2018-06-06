---
UID: NF:winsync.ICoreFragmentInspector.Reset
title: ICoreFragmentInspector::Reset
author: windows-sdk-content
description: Resets the enumerator to the beginning of the knowledge.
old-location: winsync\icorefragmentinspector_reset.htm
old-project: winsync
ms.assetid: 57621ce0-c484-4687-9f2f-98d285b041ca
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ICoreFragmentInspector interface [Windows Sync],Reset method, ICoreFragmentInspector.Reset, ICoreFragmentInspector::Reset, Reset, Reset method [Windows Sync], Reset method [Windows Sync],ICoreFragmentInspector interface, winsync.icorefragmentinspector_reset, winsync/ICoreFragmentInspector::Reset
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ICoreFragmentInspector.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ICoreFragmentInspector::Reset


## -description


Resets the enumerator to the beginning of the knowledge.


## -parameters






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
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The knowledge object that is associated with this object has changed since this object was created.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/10c22b92-bda8-42f6-9fd6-58e77e5a18d4">ICoreFragmentInspector Interface</a>
 

 

