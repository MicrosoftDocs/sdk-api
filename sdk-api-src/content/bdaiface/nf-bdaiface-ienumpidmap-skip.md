---
UID: NF:bdaiface.IEnumPIDMap.Skip
title: IEnumPIDMap::Skip method
author: windows-driver-content
description: The Skip method skips the specified number of elements in the collection.
old-location: dshow\ienumpidmap_skip.htm
old-project: DirectShow
ms.assetid: e611e5a0-beb1-4a31-974a-29b2b8349a17
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IEnumPIDMap, IEnumPIDMap interface [DirectShow], Skip method, IEnumPIDMap::Skip, IEnumPIDMapSkip, Skip method [DirectShow], Skip method [DirectShow], IEnumPIDMap interface, Skip,IEnumPIDMap.Skip, bdaiface/IEnumPIDMap::Skip, dshow.ienumpidmap_skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IEnumPIDMap.Skip
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IEnumPIDMap::Skip method


## -description



The <code>Skip</code> method skips the specified number of elements in the collection.




## -parameters




### -param cRecords [in]

Specifies the number of elements to skip.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Reached the end of the collection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d46010c4-0f16-4c97-ad10-16f7ac250390">IEnumPIDMap Interface</a>
 

 

