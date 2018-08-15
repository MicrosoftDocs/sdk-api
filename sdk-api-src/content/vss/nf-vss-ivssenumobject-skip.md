---
UID: NF:vss.IVssEnumObject.Skip
title: IVssEnumObject::Skip
author: windows-sdk-content
description: Skips the specified number of objects.
old-location: base\ivssenumobject_skip.htm
old-project: vss
ms.assetid: a655978e-49fa-445d-8576-ba82b523750c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IVssEnumObject interface [VSS],Skip method, IVssEnumObject.Skip, IVssEnumObject::Skip, Skip, Skip method [VSS], Skip method [VSS],IVssEnumObject interface, _win32_ivssenumobject_skip, base.ivssenumobject_skip, vss/IVssEnumObject::Skip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vss.h
req.include-header: 
req.redist: 
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
req.typenames: VSS_WRITER_STATE, *PVSS_WRITER_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssEnumObject.Skip
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssEnumObject::Skip


## -description


The <b>Skip</b> method skips the specified 
    number of objects.


## -parameters




### -param celt [in]

Number of elements to be skipped in the list of enumerated objects.


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
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to access a location beyond the end of the list of items.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There was an internal error in the enumerator.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a>
 

 

