---
UID: NF:bdaiface.IEnumPIDMap.Next
title: IEnumPIDMap::Next
author: windows-sdk-content
description: The Next method retrieves the next n elements in the collection.
old-location: dshow\ienumpidmap_next.htm
old-project: DirectShow
ms.assetid: e7e3a2a7-cc62-478d-b0b8-30d58f0b3372
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IEnumPIDMap interface [DirectShow],Next method, IEnumPIDMap.Next, IEnumPIDMap::Next, IEnumPIDMapNext, Next, Next method [DirectShow], Next method [DirectShow],IEnumPIDMap interface, bdaiface/IEnumPIDMap::Next, dshow.ienumpidmap_next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IEnumPIDMap.Next
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IEnumPIDMap::Next


## -description



The <code>Next</code> method retrieves the next <i>n</i> elements in the collection.




## -parameters




### -param cRequest [in]

The number of elements to retrieve.


### -param pPIDMap [in, out]

Address of an array allocated by the caller, containing <i>cRequest</i> elements. The array is filled with <a href="https://msdn.microsoft.com/c247ec75-483d-4587-a82f-07bbf6d277b4">PID_MAP</a> structures that describe the PID mapping.


### -param pcReceived [out]

Pointer to a variable that receives the number of elements actually retrieved. This parameter cannot be <b>NULL</b>. If <i>cRequest</i> equals zero, this parameter receives the total number of items in the collection.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; <i>pPidMap</i> and <i>pcReceived</i> cannot be <b>NULL</b>.

</td>
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
 

 

