---
UID: NF:qmgr.IEnumBackgroundCopyGroups.Skip
title: IEnumBackgroundCopyGroups::Skip
author: windows-sdk-content
description: Use the Skip method to skip the next specified number of elements in the enumeration sequence. If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.
old-location: bits\ienumbackgroundcopygroups_skip.htm
old-project: bits
ms.assetid: 27e907d0-1b2a-44d2-b401-0b28d5a8b340
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IEnumBackgroundCopyGroups interface [BITS],Skip method, IEnumBackgroundCopyGroups.Skip, IEnumBackgroundCopyGroups::Skip, Skip, Skip method [BITS], Skip method [BITS],IEnumBackgroundCopyGroups interface, bits.ienumbackgroundcopygroups_skip, qmgr/IEnumBackgroundCopyGroups::Skip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: qmgr.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GROUPPROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IEnumBackgroundCopyGroups.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: ADAM
---

# IEnumBackgroundCopyGroups::Skip


## -description


<p class="CCE_Message">[<b>IEnumBackgroundCopyGroups</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>Skip</b> method to skip the next specified number of elements in the enumeration sequence. If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.


## -parameters




### -param celt [in]

Number of elements to skip.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully skipped the number of requested elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Skipped less than the number of requested elements.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/64a05103-9749-41fd-9987-8bb17b9284f7">IEnumBackgroundCopyGroups</a>
 

 

