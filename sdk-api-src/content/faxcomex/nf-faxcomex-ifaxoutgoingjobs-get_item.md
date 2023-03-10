---
UID: NF:faxcomex.IFaxOutgoingJobs.get_Item
title: IFaxOutgoingJobs::get_Item (faxcomex.h)
description: The IFaxOutgoingJobs::get_Item method returns a IFaxOutgoingJob interface from the IFaxOutgoingJobs interface.
helpviewer_keywords: ["IFaxOutgoingJobs interface [Fax Service]","get_Item method","IFaxOutgoingJobs.get_Item","IFaxOutgoingJobs::get_Item","_mfax_faxoutgoingjobs.item_cpp","fax._mfax_faxoutgoingjobs_item_cpp","faxcomex/IFaxOutgoingJobs::get_Item","get_Item","get_Item method [Fax Service]","get_Item method [Fax Service]","IFaxOutgoingJobs interface"]
old-location: fax\_mfax_faxoutgoingjobs_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_63ot_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingJobs interface [Fax Service],get_Item method, IFaxOutgoingJobs.get_Item, IFaxOutgoingJobs::get_Item, _mfax_faxoutgoingjobs.item_cpp, fax._mfax_faxoutgoingjobs_item_cpp, faxcomex/IFaxOutgoingJobs::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxOutgoingJobs interface
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
 - IFaxOutgoingJobs::get_Item
 - faxcomex/IFaxOutgoingJobs::get_Item
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
 - IFaxOutgoingJobs.get_Item
---

# IFaxOutgoingJobs::get_Item


## -description

The <b>IFaxOutgoingJobs::get_Item</b> method returns a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjob">IFaxOutgoingJob</a> interface from the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjobs">IFaxOutgoingJobs</a> interface.

## -parameters

### -param vIndex [in]

Type: <b>VARIANT</b>

Variant that specifies the item to retrieve from the collection.
				



If this parameter is type VT_I2 or VT_I4, the parameter specifies the index of the item to retrieve from the collection. The index is 1-based. If this parameter is type VT_BSTR, the parameter is a job ID that specifies the outbound job to retrieve. Other types are not supported.

### -param pFaxOutgoingJob [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjob">IFaxOutgoingJob</a>**</b>

An address of a pointer that receives a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjob">IFaxOutgoingJob</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjobs">FaxOutgoingJobs</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjobs">IFaxOutgoingJobs</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outgoing-jobs">Visual Basic Example</a>