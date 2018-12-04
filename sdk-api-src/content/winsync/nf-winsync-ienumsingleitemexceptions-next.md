---
UID: NF:winsync.IEnumSingleItemExceptions.Next
title: IEnumSingleItemExceptions::Next
author: windows-sdk-content
description: Returns the next elements in the single-item exception set, if they are available.
old-location: winsync\ienumsingleitemexceptions_next.htm
tech.root: winsync
ms.assetid: a9605eaa-2b68-4bc6-9dcf-c2bebc4e6f1b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IEnumSingleItemExceptions interface [Windows Sync],Next method, IEnumSingleItemExceptions.Next, IEnumSingleItemExceptions::Next, Next, Next method [Windows Sync], Next method [Windows Sync],IEnumSingleItemExceptions interface, winsync.ienumsingleitemexceptions_next, winsync/IEnumSingleItemExceptions::Next
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
 - IEnumSingleItemExceptions.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumSingleItemExceptions::Next


## -description


Returns the next elements in the single-item exception set, if they are available.


## -parameters




### -param cExceptions [in]

The number of single-item exceptions to retrieve in the range from zero to 1000.


### -param ppSingleItemException [out]

Returns the next <i>pcFetched</i> single-item exceptions.


### -param pcFetched [in, out]

Returns the number of single-item exceptions returned. This value can be <b>NULL</b> only if <i>cExceptions</i> is 1.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no more single-item exceptions to retrieve.

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
 




## -see-also




<a href="https://msdn.microsoft.com/fed8a258-bc23-454b-9d8a-e3873481b33b">IEnumSingleItemExceptions Interface</a>
 

 

