---
UID: NF:faxcomex.IFaxIncomingQueue.Save
title: IFaxIncomingQueue::Save (faxcomex.h)
description: The Save method saves the FaxIncomingQueue object's data.
helpviewer_keywords: ["IFaxIncomingQueue interface [Fax Service]","Save method","IFaxIncomingQueue.Save","IFaxIncomingQueue::Save","Save","Save method [Fax Service]","Save method [Fax Service]","IFaxIncomingQueue interface","_mfax_faxincomingqueue.save","fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_save_cpp","fax._mfax_faxincomingqueue_save","faxcomex/IFaxIncomingQueue::Save"]
old-location: fax\_mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_save_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_2m3p.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingQueue interface [Fax Service],Save method, IFaxIncomingQueue.Save, IFaxIncomingQueue::Save, Save, Save method [Fax Service], Save method [Fax Service],IFaxIncomingQueue interface, _mfax_faxincomingqueue.save, fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_save_cpp, fax._mfax_faxincomingqueue_save, faxcomex/IFaxIncomingQueue::Save
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
 - IFaxIncomingQueue::Save
 - faxcomex/IFaxIncomingQueue::Save
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
 - IFaxIncomingQueue.Save
 - IFaxIncomingQueue.Save
---

# IFaxIncomingQueue::Save


## -description

The <b>Save</b> method saves the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingqueue">FaxIncomingQueue</a> object's data.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> and <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access rights.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingqueue">FaxIncomingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingqueue">IFaxIncomingQueue</a>
