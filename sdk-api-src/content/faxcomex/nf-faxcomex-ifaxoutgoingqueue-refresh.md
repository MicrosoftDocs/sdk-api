---
UID: NF:faxcomex.IFaxOutgoingQueue.Refresh
title: IFaxOutgoingQueue::Refresh (faxcomex.h)
description: The IFaxOutgoingQueue::Refresh method refreshes FaxOutgoingQueue object information from the fax server. When the IFaxOutgoingQueue::Refresh method is called, any configuration changes made after the last IFaxOutgoingQueue::Save method call are lost.
helpviewer_keywords: ["IFaxOutgoingQueue interface [Fax Service]","Refresh method","IFaxOutgoingQueue.Refresh","IFaxOutgoingQueue::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxOutgoingQueue interface","_mfax_faxoutgoingqueue.refresh","fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_refresh_cpp","fax._mfax_faxoutgoingqueue_refresh","faxcomex/IFaxOutgoingQueue::Refresh"]
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4my0.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingQueue interface [Fax Service],Refresh method, IFaxOutgoingQueue.Refresh, IFaxOutgoingQueue::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxOutgoingQueue interface, _mfax_faxoutgoingqueue.refresh, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_refresh_cpp, fax._mfax_faxoutgoingqueue_refresh, faxcomex/IFaxOutgoingQueue::Refresh
req.header: faxcomex.h
req.include-header: 
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxOutgoingQueue::Refresh
 - faxcomex/IFaxOutgoingQueue::Refresh
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingQueue.Refresh
 - IFaxOutgoingQueue.Refresh
---

# IFaxOutgoingQueue::Refresh


## -description

The <b>IFaxOutgoingQueue::Refresh</b> method refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a> object information from the fax server. When the <b>IFaxOutgoingQueue::Refresh</b> method is called, any configuration changes made after the last <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-save-vb">IFaxOutgoingQueue::Save</a> method call are lost.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingqueue">IFaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outgoing-jobs">Managing Outgoing Jobs</a>
