---
UID: NN:objidl.IFillLockBytes
title: IFillLockBytes
author: windows-sdk-content
description: The IFillLockBytes interface enables downloading code to write data asynchronously to a structured storage byte array.
old-location: stg\ifilllockbytes.htm
old-project: Stg
ms.assetid: 033b3db4-3ff0-4cb4-916f-2490e92f5e6a
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IFillLockBytes, IFillLockBytes interface [Structured Storage], IFillLockBytes interface [Structured Storage],described, _stg_ifilllockbytes, objidl/IFillLockBytes, stg.ifilllockbytes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	IFillLockBytes
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IFillLockBytes interface


## -description



			The 
<b>IFillLockBytes</b> interface enables downloading code to write data asynchronously to a structured storage byte array. When the downloading code has new data available, it calls 
<a href="https://msdn.microsoft.com/3f25c48f-85a4-4778-b262-ad0c52cb1ac9">IFillLockBytes::FillAppend</a> or <a href="https://msdn.microsoft.com/d378d87b-e081-4950-b87b-9b1ad6dfb29d">IFillLockBytes::FillAt</a> to write the data to the byte array. An application attempting to access this data, through calls to the 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> interface, can do so even as the downloader continues to make calls to 
<b>IFillLockBytes</b>. If the application attempts to access data that has not already been downloaded through a call to 
<b>IFillLockBytes</b>, then 
<b>ILockBytes</b> returns a new error, E_PENDING.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFillLockBytes</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFillLockBytes</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFillLockBytes</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f25c48f-85a4-4778-b262-ad0c52cb1ac9">FillAppend</a>
</td>
<td align="left" width="63%">
Writes a new block of bytes to end of byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d378d87b-e081-4950-b87b-9b1ad6dfb29d">FillAt</a>
</td>
<td align="left" width="63%">
Writes a new block of bytes to specified location in byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1336079e-02d2-4799-a58f-d097ec80c03b">SetFillSize</a>
</td>
<td align="left" width="63%">
Sets expected size of byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21ea78c7-51f1-4418-915c-79db47c25715">Terminate</a>
</td>
<td align="left" width="63%">
Notifies byte array wrapper of successful or unsuccessful termination of download.

</td>
</tr>
</table> 


## -see-also




<a href="ie.BINDINFO_Structure">BINDINFO</a>



<a href="_com_iconnectionpoint">IConnectionPoint</a>



<a href="_com_iconnectionpointcontainer">IConnectionPointContainer</a>



<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a>



<a href="_com_iprogressnotify">IProgressNotify</a>



<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>



<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>
 

 

