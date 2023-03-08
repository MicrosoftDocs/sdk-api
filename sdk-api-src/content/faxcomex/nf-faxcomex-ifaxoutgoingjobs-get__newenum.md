---
UID: NF:faxcomex.IFaxOutgoingJobs.get__NewEnum
title: IFaxOutgoingJobs::get__NewEnum (faxcomex.h)
description: The IFaxOutgoingJobs::get__NewEnum method returns a reference to an enumerator object that you can use to iterate through the IFaxOutgoingJobs collection.
helpviewer_keywords: ["IFaxOutgoingJobs interface [Fax Service]","get__NewEnum method","IFaxOutgoingJobs.get__NewEnum","IFaxOutgoingJobs::get__NewEnum","_mfax_ifaxoutgoingjobs_get__newenum","fax._mfax_ifaxoutgoingjobs_get__newenum","faxcomex/IFaxOutgoingJobs::get__NewEnum","get__NewEnum","get__NewEnum method [Fax Service]","get__NewEnum method [Fax Service]","IFaxOutgoingJobs interface"]
old-location: fax\_mfax_ifaxoutgoingjobs_get__newenum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_306l.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingJobs interface [Fax Service],get__NewEnum method, IFaxOutgoingJobs.get__NewEnum, IFaxOutgoingJobs::get__NewEnum, _mfax_ifaxoutgoingjobs_get__newenum, fax._mfax_ifaxoutgoingjobs_get__newenum, faxcomex/IFaxOutgoingJobs::get__NewEnum, get__NewEnum, get__NewEnum method [Fax Service], get__NewEnum method [Fax Service],IFaxOutgoingJobs interface
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
 - IFaxOutgoingJobs::get__NewEnum
 - faxcomex/IFaxOutgoingJobs::get__NewEnum
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
 - IFaxOutgoingJobs.get__NewEnum
---

# IFaxOutgoingJobs::get__NewEnum


## -description

The <b>IFaxOutgoingJobs::get__NewEnum</b> method returns a reference to an enumerator object that you can use to iterate through the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjobs">IFaxOutgoingJobs</a> collection.

## -parameters

### -param ppUnk [out, retval]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

Receives an indirect pointer to the enumerator object's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface for this collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjobs">FaxOutgoingJobs</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingjobs">IFaxOutgoingJobs</a>