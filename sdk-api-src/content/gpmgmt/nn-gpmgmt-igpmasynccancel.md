---
UID: NN:gpmgmt.IGPMAsyncCancel
title: IGPMAsyncCancel (gpmgmt.h)
author: windows-sdk-content
description: A pointer to the IGPMAsyncCancel interface is returned to the client by the Group Policy Management Console (GPMC) method that the client calls asynchronously.
old-location: gpmc\igpmasynccancel.htm
tech.root: gpmc
ms.assetid: 74b2bb04-6118-4fd1-83c0-3549db3f35f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMAsyncCancel, IGPMAsyncCancel, IGPMAsyncCancel interface [GPMC], IGPMAsyncCancel interface [GPMC],described, _win32_igpmasynccancel, gpmc.igpmasynccancel, gpmgmt/IGPMAsyncCancel
ms.topic: interface
f1_keywords: 
 - "gpmgmt/IGPMAsyncCancel"
dev_langs:
 - c++
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMAsyncCancel
 - GPMAsyncCancel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMAsyncCancel interface


## -description


A pointer to the 
<b>IGPMAsyncCancel</b> interface is returned to the client by the Group Policy Management Console (GPMC) method that the client calls asynchronously. GPMC operations such as backup, restore, import, copy, and report generation can execute asynchronously. This object cannot be accessed through scripting.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMAsyncCancel</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMAsyncCancel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGPMAsyncCancel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmasynccancel-cancel">Cancel</a>
</td>
<td align="left" width="63%">
A client application calls this function to cancel a GPMC operation.

</td>
</tr>
</table> 


## -remarks



GPMC operations such as backup, restore, import, copy, and report generation can execute asynchronously. For more information about how to use this interface with asynchronous operations, see the "Remarks" section of 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress Interface</a>. The server calls 
the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmasyncprogress-status">IGPMAsyncProgress::Status</a> method to notify the client about the progress of the operation. The 
<b>Status</b> method also returns an interface pointer to the resultant object, for example, to a <b>GPMGPO</b> or to a <b>GPMBackup</b> object. The caller can then cancel the operation by calling the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmasynccancel-cancel">IGPMAsyncCancel::Cancel</a> method.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a>
 

 

