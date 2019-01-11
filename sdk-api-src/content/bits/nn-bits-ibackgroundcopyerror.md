---
UID: NN:bits.IBackgroundCopyError
title: IBackgroundCopyError
author: windows-sdk-content
description: Use the IBackgroundCopyError interface to determine the cause of an error and if the transfer process can proceed.
old-location: bits\ibackgroundcopyerror.htm
tech.root: Bits
ms.assetid: a0b9e887-84d5-4f67-a65c-6a807c50dafd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBackgroundCopyError, IBackgroundCopyError interface [BITS], IBackgroundCopyError interface [BITS],described, _drz_ibackgroundcopyerror, bits.ibackgroundcopyerror, bits/IBackgroundCopyError
ms.topic: interface
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyError interface


## -description


Use the  
<b>IBackgroundCopyError</b> interface to determine the cause of 	an  error and if the transfer process can proceed.

BITS creates an error object only when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR. BITS does not create an error object when an <b>IBackgroundCopyXXXX</b> interface method fails. The error object is available until BITS begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job or until your application exits.

To get an 
<b>IBackgroundCopyError</b> object, call the 
<a href="https://msdn.microsoft.com/2ad4c913-2d1e-4490-968c-960178a57e3b">IBackgroundCopyJob::GetError</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyError</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBackgroundCopyError</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyError</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abdf115d-3ff2-4664-b053-f55872ad24ab">GetError</a>
</td>
<td align="left" width="63%">
Retrieves the error code and identifies the context in which the error occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87f5ae62-c171-4637-bebb-3a5c5aa546b3">GetErrorContextDescription</a>
</td>
<td align="left" width="63%">
Retrieves a description of the context in which the error occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57323f38-c2e6-4e40-b357-7df758899f97">GetErrorDescription</a>
</td>
<td align="left" width="63%">
Retrieves the error text associated with the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b6d4bd4-2102-4e6b-b250-1d73fae94cf9">GetFile</a>
</td>
<td align="left" width="63%">
Retrieves an interface pointer to the file object associated with the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94c1fcc8-7132-41db-9a1c-cbe105e3b0bb">GetProtocol</a>
</td>
<td align="left" width="63%">
Retrieves the protocol used to transfer the file.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a7857cf1-05b7-42df-b79e-50a2f6a406dc">BG_JOB_STATE</a>



<a href="https://msdn.microsoft.com/3e206195-1a8c-435e-9b8f-6517b8e3c4ca">IBackgroundCopyCallback::JobError</a>



<a href="https://msdn.microsoft.com/2ad4c913-2d1e-4490-968c-960178a57e3b">IBackgroundCopyJob::GetError</a>



<a href="https://msdn.microsoft.com/32789bd2-2368-473b-accf-ac6e317d0172">IBackgroundCopyJob::GetState</a>



<a href="https://msdn.microsoft.com/e62e2bde-485d-42d4-b824-a682ab9e16ca">IBackgroundCopyManager::GetErrorDescription</a>
 

 

