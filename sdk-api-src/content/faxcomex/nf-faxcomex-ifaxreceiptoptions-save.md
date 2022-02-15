---
UID: NF:faxcomex.IFaxReceiptOptions.Save
title: IFaxReceiptOptions::Save (faxcomex.h)
description: The IFaxReceiptOptions::Save method saves the FaxReceiptOptions object data.
helpviewer_keywords: ["IFaxReceiptOptions interface [Fax Service]","Save method","IFaxReceiptOptions.Save","IFaxReceiptOptions::Save","Save","Save method [Fax Service]","Save method [Fax Service]","IFaxReceiptOptions interface","_mfax_faxreceiptoptions.save","fax._mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_save_cpp","fax._mfax_faxreceiptoptions_save","faxcomex/IFaxReceiptOptions::Save"]
old-location: fax\_mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_save_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_25ph.htm
ms.date: 12/05/2018
ms.keywords: IFaxReceiptOptions interface [Fax Service],Save method, IFaxReceiptOptions.Save, IFaxReceiptOptions::Save, Save, Save method [Fax Service], Save method [Fax Service],IFaxReceiptOptions interface, _mfax_faxreceiptoptions.save, fax._mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_save_cpp, fax._mfax_faxreceiptoptions_save, faxcomex/IFaxReceiptOptions::Save
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
 - IFaxReceiptOptions::Save
 - faxcomex/IFaxReceiptOptions::Save
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
 - IFaxReceiptOptions.Save
 - IFaxReceiptOptions.Save
---

# IFaxReceiptOptions::Save


## -description

The <b>IFaxReceiptOptions::Save</b> method saves the <a href="/previous-versions/windows/desktop/fax/-mfax-faxreceiptoptions">FaxReceiptOptions</a> object data.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is not supported for Windows XP when the receipt type is set to <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_receipt_type_enum">frtMAIL</a>, or if <a href="/previous-versions/windows/desktop/fax/-mfax-faxreceiptoptions-useforinboundrouting-vb">IFaxReceiptOptions::get_UseForInboundRouting </a> is set to <b>TRUE</b>. In these cases, this method will return the error: <a href="/previous-versions/windows/desktop/fax/-mfax-fax-error-codes">FAX_E_NOT_SUPPORTED_ON_THIS_SKU</a>.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> and <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access rights.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxreceiptoptions">FaxReceiptOptions</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxreceiptoptions">IFaxReceiptOptions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-receipt-options">Setting Receipt Options</a>
