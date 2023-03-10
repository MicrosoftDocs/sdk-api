---
UID: NF:faxcomex.IFaxDeviceIds.get__NewEnum
title: IFaxDeviceIds::get__NewEnum (faxcomex.h)
description: The IFaxDeviceIds::get__NewEnum method returns a reference to an enumerator object that you can use to iterate through the FaxDeviceIds collection.
helpviewer_keywords: ["IFaxDeviceIds interface [Fax Service]","get__NewEnum method","IFaxDeviceIds.get__NewEnum","IFaxDeviceIds::get__NewEnum","_mfax_ifaxdeviceids_get__newenum","fax._mfax_ifaxdeviceids_get__newenum","faxcomex/IFaxDeviceIds::get__NewEnum","get__NewEnum","get__NewEnum method [Fax Service]","get__NewEnum method [Fax Service]","IFaxDeviceIds interface"]
old-location: fax\_mfax_ifaxdeviceids_get__newenum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4gj1.htm
ms.date: 12/05/2018
ms.keywords: IFaxDeviceIds interface [Fax Service],get__NewEnum method, IFaxDeviceIds.get__NewEnum, IFaxDeviceIds::get__NewEnum, _mfax_ifaxdeviceids_get__newenum, fax._mfax_ifaxdeviceids_get__newenum, faxcomex/IFaxDeviceIds::get__NewEnum, get__NewEnum, get__NewEnum method [Fax Service], get__NewEnum method [Fax Service],IFaxDeviceIds interface
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
 - IFaxDeviceIds::get__NewEnum
 - faxcomex/IFaxDeviceIds::get__NewEnum
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
 - IFaxDeviceIds.get__NewEnum
---

# IFaxDeviceIds::get__NewEnum


## -description

The <b>IFaxDeviceIds::get__NewEnum</b> method returns a reference to an enumerator object that you can use to iterate through the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a> collection.

## -parameters

### -param ppUnk [out, retval]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

Receives an indirect pointer to the enumerator object's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface for the collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In Microsoft Visual Basic, you do not need to use the corresponding <b>_NewEnum</b> property, because it is automatically used in the implementation of <b>For Each ... Next</b>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceids">IFaxDeviceIds</a>