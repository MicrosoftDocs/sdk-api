---
UID: NN:imapi2.IDiscFormat2DataEventArgs
title: IDiscFormat2DataEventArgs
author: windows-sdk-content
description: Use this interface to retrieve information about the current write operation.
old-location: imapi\idiscformat2dataeventargs.htm
tech.root: imapi
ms.assetid: 6bf149d3-62ea-4ef5-8d45-44df9ad4982c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiscFormat2DataEventArgs, IDiscFormat2DataEventArgs interface [IMAPI], IDiscFormat2DataEventArgs interface [IMAPI],described, imapi.idiscformat2dataeventargs, imapi2/IDiscFormat2DataEventArgs
ms.topic: interface
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IDiscFormat2DataEventArgs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2DataEventArgs interface


## -description


Use this interface to retrieve information about the current write operation. 

This interface is passed to the <a href="https://msdn.microsoft.com/786fc936-9493-4cc3-a937-4d1f4b54fe88">DDiscFormat2DataEvents::Update</a> method that you implement.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscFormat2DataEventArgs</b> interface inherits from <a href="https://msdn.microsoft.com/1922410a-5871-477f-b778-36b12ad95168">IWriteEngine2EventArgs</a>. <b>IDiscFormat2DataEventArgs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscFormat2DataEventArgs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad7db1a4-7ea8-46d7-8c4f-e7b9fb232f63">get_CurrentAction</a>
</td>
<td align="left" width="63%">
Retrieves the current write action being performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ac3c261-dedc-4316-9241-387fc222443d">get_ElapsedTime</a>
</td>
<td align="left" width="63%">
Retrieves the total elapsed time of the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fc41d22-c85b-47dc-8d09-a8d135cfe95e">get_RemainingTime</a>
</td>
<td align="left" width="63%">
Retrieves the estimated remaining time of the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95e61ef9-5d1c-4f29-896f-69a56c23f306">get_TotalTime</a>
</td>
<td align="left" width="63%">
Retrieves the estimated total time for write operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f9f1d976-9ec9-40a5-92b6-d00a7e15d0aa">DDiscFormat2DataEvents</a>



<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/1922410a-5871-477f-b778-36b12ad95168">IWriteEngine2EventArgs</a>
 

 

