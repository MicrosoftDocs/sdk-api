---
UID: NF:faxcomex.IFaxOutgoingQueue.Save
title: IFaxOutgoingQueue::Save (faxcomex.h)
description: The IFaxOutgoingQueue::Save method saves the FaxOutgoingQueue object data.
helpviewer_keywords: ["IFaxOutgoingQueue interface [Fax Service]","Save method","IFaxOutgoingQueue.Save","IFaxOutgoingQueue::Save","Save","Save method [Fax Service]","Save method [Fax Service]","IFaxOutgoingQueue interface","_mfax_faxoutgoingqueue.save","fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_save_cpp","fax._mfax_faxoutgoingqueue_save","faxcomex/IFaxOutgoingQueue::Save"]
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_save_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_486d.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingQueue interface [Fax Service],Save method, IFaxOutgoingQueue.Save, IFaxOutgoingQueue::Save, Save, Save method [Fax Service], Save method [Fax Service],IFaxOutgoingQueue interface, _mfax_faxoutgoingqueue.save, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_save_cpp, fax._mfax_faxoutgoingqueue_save, faxcomex/IFaxOutgoingQueue::Save
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
 - IFaxOutgoingQueue::Save
 - faxcomex/IFaxOutgoingQueue::Save
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
 - IFaxOutgoingQueue.Save
 - IFaxOutgoingQueue.Save
---

# IFaxOutgoingQueue::Save


## -description

The <b>IFaxOutgoingQueue::Save</b> method saves the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a> object data.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> or <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingqueue">IFaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-the-outgoing-queue-properties">Setting the Outgoing Queue Properties</a>
