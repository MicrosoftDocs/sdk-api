---
UID: NN:bits.IBackgroundCopyError
title: IBackgroundCopyError (bits.h)
description: Use the IBackgroundCopyError interface to determine the cause of an error and if the transfer process can proceed.
helpviewer_keywords: ["IBackgroundCopyError","IBackgroundCopyError interface [BITS]","IBackgroundCopyError interface [BITS]","described","_drz_ibackgroundcopyerror","bits.ibackgroundcopyerror","bits/IBackgroundCopyError"]
old-location: bits\ibackgroundcopyerror.htm
tech.root: Bits
ms.assetid: a0b9e887-84d5-4f67-a65c-6a807c50dafd
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyError, IBackgroundCopyError interface [BITS], IBackgroundCopyError interface [BITS],described, _drz_ibackgroundcopyerror, bits.ibackgroundcopyerror, bits/IBackgroundCopyError
f1_keywords:
- bits/IBackgroundCopyError
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBackgroundCopyError interface


## -description


Use the  
<b>IBackgroundCopyError</b> interface to determine the cause of 	an  error and if the transfer process can proceed.

BITS creates an error object only when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR. BITS does not create an error object when an <b>IBackgroundCopyXXXX</b> interface method fails. The error object is available until BITS begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job or until your application exits.

To get an 
<b>IBackgroundCopyError</b> object, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-geterror">IBackgroundCopyJob::GetError</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyError</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyError</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-geterror">GetError</a>
</td>
<td align="left" width="63%">
Retrieves the error code and identifies the context in which the error occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-geterrorcontextdescription">GetErrorContextDescription</a>
</td>
<td align="left" width="63%">
Retrieves a description of the context in which the error occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-geterrordescription">GetErrorDescription</a>
</td>
<td align="left" width="63%">
Retrieves the error text associated with the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-getfile">GetFile</a>
</td>
<td align="left" width="63%">
Retrieves an interface pointer to the file object associated with the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-getprotocol">GetProtocol</a>
</td>
<td align="left" width="63%">
Retrieves the protocol used to transfer the file.

</td>
</tr>
</table> 


## -see-also




<a href="/windows/desktop/api/bits/ne-bits-bg_job_state">BG_JOB_STATE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopycallback-joberror">IBackgroundCopyCallback::JobError</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-geterror">IBackgroundCopyJob::GetError</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getstate">IBackgroundCopyJob::GetState</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-geterrordescription">IBackgroundCopyManager::GetErrorDescription</a>
 

 

