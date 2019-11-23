---
UID: NN:bits.IBackgroundCopyManager
title: IBackgroundCopyManager (bits.h)

description: Creates transfer jobs, retrieves an enumerator object that contains the jobs in the queue, and retrieves individual jobs from the queue.
old-location: bits\ibackgroundcopymanager.htm
tech.root: Bits
ms.assetid: fc98dfb3-7e10-421d-b722-223bd8a65330

ms.date: 12/05/2018
ms.keywords: IBackgroundCopyManager, IBackgroundCopyManager interface [BITS], IBackgroundCopyManager interface [BITS],described, _drz_ibackgroundcopymanager, bits.ibackgroundcopymanager, bits/IBackgroundCopyManager
ms.topic: interface
f1_keywords: 
 - "bits/IBackgroundCopyManager"
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
 - IBackgroundCopyManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBackgroundCopyManager interface


## -description


Creates transfer jobs, retrieves an enumerator object that contains the jobs in the queue, and retrieves individual jobs from the queue.

For information on how to create an instance of this interface, see 
<a href="https://docs.microsoft.com/windows/desktop/Bits/connecting-to-the-bits-service">Connecting to the BITS Service</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-createjob">CreateJob</a>
</td>
<td align="left" width="63%">
Creates a transfer job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-enumjobs">EnumJobs</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator object that you use to enumerate jobs in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-geterrordescription">GetErrorDescription</a>
</td>
<td align="left" width="63%">
Retrieves a description for the specified error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-getjob">GetJob</a>
</td>
<td align="left" width="63%">
Retrieves a specified job from the queue.

</td>
</tr>
</table> 


## -remarks



<b>Windows Vista and later:  </b>When an ActiveX control tries to instantiate this interface from an Internet Explorer process, the call will fail with access denied. This is because COM does not allow lower-integrity clients to bind to class instances at higher integrity levels. For details, see <a href="http://go.microsoft.com/fwlink/p/?linkid=103101">Understanding and Working in Protected Mode Internet Explorer</a> and <a href="http://go.microsoft.com/fwlink/p/?linkid=103102">How the Integrity Mechanism Is Implemented in Windows Vista</a>. A user can workaround the issue by adding the website to the Trusted site zone.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyjobs">IEnumBackgroundCopyJobs</a>
 

 

