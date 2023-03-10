---
UID: NF:faxcomex.IFaxIncomingQueue.Refresh
title: IFaxIncomingQueue::Refresh (faxcomex.h)
description: The Refresh method refreshes FaxIncomingQueue object information from the fax server. When the Refresh method is called, any configuration changes made after the last Save method call are lost.
helpviewer_keywords: ["IFaxIncomingQueue interface [Fax Service]","Refresh method","IFaxIncomingQueue.Refresh","IFaxIncomingQueue::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxIncomingQueue interface","_mfax_faxincomingqueue.refresh","fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_refresh_cpp","fax._mfax_faxincomingqueue_refresh","faxcomex/IFaxIncomingQueue::Refresh"]
old-location: fax\_mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_24vc.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingQueue interface [Fax Service],Refresh method, IFaxIncomingQueue.Refresh, IFaxIncomingQueue::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxIncomingQueue interface, _mfax_faxincomingqueue.refresh, fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_refresh_cpp, fax._mfax_faxincomingqueue_refresh, faxcomex/IFaxIncomingQueue::Refresh
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
 - IFaxIncomingQueue::Refresh
 - faxcomex/IFaxIncomingQueue::Refresh
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
 - IFaxIncomingQueue.Refresh
 - IFaxIncomingQueue.Refresh
---

# IFaxIncomingQueue::Refresh


## -description

The <b>Refresh</b> method refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingqueue">FaxIncomingQueue</a> object information from the fax server. When the <b>Refresh</b> method is called, any configuration changes made after the last <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingqueue-save-vb">Save</a> method call are lost.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingqueue">FaxIncomingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingqueue">IFaxIncomingQueue</a>
