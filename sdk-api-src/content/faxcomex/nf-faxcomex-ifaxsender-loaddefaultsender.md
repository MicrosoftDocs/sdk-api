---
UID: NF:faxcomex.IFaxSender.LoadDefaultSender
title: IFaxSender::LoadDefaultSender (faxcomex.h)
description: The IFaxSender::get_LoadDefaultSender method fills the FaxSender object with the default sender information.
helpviewer_keywords: ["IFaxSender interface [Fax Service]","LoadDefaultSender method","IFaxSender.LoadDefaultSender","IFaxSender::LoadDefaultSender","LoadDefaultSender","LoadDefaultSender method [Fax Service]","LoadDefaultSender method [Fax Service]","IFaxSender interface","_mfax_faxsender.loaddefaultsender","fax._mfax_faxsender_cpp_mfax_faxsender_loaddefaultsender_cpp","fax._mfax_faxsender_loaddefaultsender","faxcomex/IFaxSender::LoadDefaultSender"]
old-location: fax\_mfax_faxsender_cpp_mfax_faxsender_loaddefaultsender_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_9ak2.htm
ms.date: 12/05/2018
ms.keywords: IFaxSender interface [Fax Service],LoadDefaultSender method, IFaxSender.LoadDefaultSender, IFaxSender::LoadDefaultSender, LoadDefaultSender, LoadDefaultSender method [Fax Service], LoadDefaultSender method [Fax Service],IFaxSender interface, _mfax_faxsender.loaddefaultsender, fax._mfax_faxsender_cpp_mfax_faxsender_loaddefaultsender_cpp, fax._mfax_faxsender_loaddefaultsender, faxcomex/IFaxSender::LoadDefaultSender
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
 - IFaxSender::LoadDefaultSender
 - faxcomex/IFaxSender::LoadDefaultSender
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
 - IFaxSender.LoadDefaultSender
 - IFaxSender.LoadDefaultSender
---

# IFaxSender::LoadDefaultSender


## -description

The <b>IFaxSender::get_LoadDefaultSender</b> method fills the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsender">FaxSender</a> object with the default sender information.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default sender information is saved using the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsender-savedefaultsender-vb">IFaxSender::SaveDefaultSender</a> method.

This method can return remote procedure call (RPC) return values. For more information, see <a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxsender">FaxSender</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxsender">IFaxSender</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-broadcasting-a-fax">Visual Basic Example</a>
