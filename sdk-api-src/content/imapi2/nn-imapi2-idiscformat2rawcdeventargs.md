---
UID: NN:imapi2.IDiscFormat2RawCDEventArgs
title: IDiscFormat2RawCDEventArgs
author: windows-sdk-content
description: Use this interface to retrieve information about the current write operation.
old-location: imapi\idiscformat2rawcdeventargs.htm
tech.root: imapi
ms.assetid: b1988883-459c-46f1-a0d1-df9500a000e1
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IDiscFormat2RawCDEventArgs, IDiscFormat2RawCDEventArgs interface [IMAPI], IDiscFormat2RawCDEventArgs interface [IMAPI],described, imapi.idiscformat2rawcdeventargs, imapi2/IDiscFormat2RawCDEventArgs
ms.prod: windows
ms.technology: windows-sdk
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
 - IDiscFormat2RawCDEventArgs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2RawCDEventArgs interface


## -description


Use this interface to retrieve information about the current write operation. 

This interface is passed to the <a href="https://msdn.microsoft.com/abe35eee-63a4-4109-8927-825f86b6e302">DDiscFormat2RawCDEvents::Update</a> method that you implement.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscFormat2RawCDEventArgs</b> interface inherits from <a href="https://msdn.microsoft.com/1922410a-5871-477f-b778-36b12ad95168">IWriteEngine2EventArgs</a>. <b>IDiscFormat2RawCDEventArgs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscFormat2RawCDEventArgs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a29f77e-e895-4cb0-b1f0-83df07931893">get_CurrentAction</a>
</td>
<td align="left" width="63%">
Retrieves the current write action being performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87a1b606-f91b-4a14-b3b0-17d224d841fc">get_ElapsedTime</a>
</td>
<td align="left" width="63%">
Retrieves the total elapsed time of the write operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0dad0ca9-2ddb-44ef-ab8b-a0f0efc3634a">get_RemainingTime</a>
</td>
<td align="left" width="63%">
Retrieves the estimated remaining time of the write operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3a06911e-8a50-4e41-874c-478ad05f6488">DDiscFormat2RawCDEvents</a>



<a href="https://msdn.microsoft.com/1922410a-5871-477f-b778-36b12ad95168">IWriteEngine2EventArgs</a>
 

 

