---
UID: NF:rend.IEnumDirectoryObject.Skip
title: IEnumDirectoryObject::Skip
author: windows-sdk-content
description: The Skip method skips over the next specified number of elements in the enumeration sequence.
old-location: tapi3\ienumdirectoryobject_skip.htm
tech.root: Tapi
ms.assetid: e14e71f1-5151-4562-bfbf-1370f65cb23a
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IEnumDirectoryObject interface [TAPI 2.2],Skip method, IEnumDirectoryObject.Skip, IEnumDirectoryObject::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumDirectoryObject interface, _tapi3_ienumdirectoryobject_skip, rend/IEnumDirectoryObject::Skip, tapi3.ienumdirectoryobject_skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Rend.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - IEnumDirectoryObject.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumDirectoryObject::Skip


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Skip</b> method skips over the next specified number of elements in the enumeration sequence.


## -parameters




### -param celt [in]

Number of elements to skip.


## -returns



This method can return one of these values.

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
Number of elements skipped was <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements skipped was not <i>celt</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/328183cd-a80b-4f1f-9e5e-9f466a4e4b43">IEnumDirectoryObject</a>
 

 

