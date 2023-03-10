---
UID: NF:faxcomex.IFaxIncomingJobs.get_Item
title: IFaxIncomingJobs::get_Item (faxcomex.h)
description: Retrieves a FaxIncomingJob object from the FaxIncomingJobs collection.
helpviewer_keywords: ["IFaxIncomingJobs interface [Fax Service]","get_Item method","IFaxIncomingJobs.get_Item","IFaxIncomingJobs::get_Item","_mfax_faxincomingjobs.item_cpp","fax._mfax_faxincomingjobs_item_cpp","faxcomex/IFaxIncomingJobs::get_Item","get_Item","get_Item method [Fax Service]","get_Item method [Fax Service]","IFaxIncomingJobs interface"]
old-location: fax\_mfax_faxincomingjobs_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5ga5_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingJobs interface [Fax Service],get_Item method, IFaxIncomingJobs.get_Item, IFaxIncomingJobs::get_Item, _mfax_faxincomingjobs.item_cpp, fax._mfax_faxincomingjobs_item_cpp, faxcomex/IFaxIncomingJobs::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxIncomingJobs interface
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
 - IFaxIncomingJobs::get_Item
 - faxcomex/IFaxIncomingJobs::get_Item
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
 - IFaxIncomingJobs.get_Item
---

# IFaxIncomingJobs::get_Item


## -description

Retrieves a <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object from the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjobs">FaxIncomingJobs</a> collection.

## -parameters

### -param vIndex [in]

Type: <b>VARIANT</b>

<b>VARIANT</b> that specifies a value that indicates the item to retrieve from the collection. If this parameter is type <b>VT_I2</b> or <b>VT_I4</b>, it specifies the index of the item to retrieve. The index is 1-based. If this parameter is type <b>VT_BSTR</b>, it specifies a job ID to use to search the collection. Other types are not supported.

### -param pFaxIncomingJob [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjob">IFaxIncomingJob</a>**</b>

Receives an indirect pointer to a <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjobs">IFaxIncomingJobs</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjobs-item">Item</a>