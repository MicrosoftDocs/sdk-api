---
UID: NF:strmif.IDvdState.GetDiscID
title: IDvdState::GetDiscID
author: windows-sdk-content
description: The GetDiscID method retrieves the unique ID of the disc from which the bookmark was made.
old-location: dshow\idvdstate_getdiscid.htm
tech.root: DirectShow
ms.assetid: 1a3d8dba-4281-4385-b48f-d9d1b1134676
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDiscID, GetDiscID method [DirectShow], GetDiscID method [DirectShow],IDvdState interface, IDvdState interface [DirectShow],GetDiscID method, IDvdState.GetDiscID, IDvdState::GetDiscID, IDvdStateGetDiscID, dshow.idvdstate_getdiscid, strmif/IDvdState::GetDiscID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdState.GetDiscID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdState::GetDiscID


## -description



The <code>GetDiscID</code> method retrieves the unique ID of the disc from which the bookmark was made.




## -parameters




### -param pullUniqueID [out]

Receives the ID.


## -returns



Returns one of the values shown in the following table.

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
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/df30a3b9-7541-42a8-b642-3b6450a0345e">IDvdState Interface</a>
 

 

