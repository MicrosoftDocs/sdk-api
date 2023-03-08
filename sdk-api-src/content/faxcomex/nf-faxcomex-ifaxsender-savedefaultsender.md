---
UID: NF:faxcomex.IFaxSender.SaveDefaultSender
title: IFaxSender::SaveDefaultSender (faxcomex.h)
description: The IFaxSender::SaveDefaultSender method stores information about the default sender from the FaxSender object.
helpviewer_keywords: ["IFaxSender interface [Fax Service]","SaveDefaultSender method","IFaxSender.SaveDefaultSender","IFaxSender::SaveDefaultSender","SaveDefaultSender","SaveDefaultSender method [Fax Service]","SaveDefaultSender method [Fax Service]","IFaxSender interface","_mfax_faxsender.savedefaultsender","fax._mfax_faxsender_cpp_mfax_faxsender_savedefaultsender_cpp","fax._mfax_faxsender_savedefaultsender","faxcomex/IFaxSender::SaveDefaultSender"]
old-location: fax\_mfax_faxsender_cpp_mfax_faxsender_savedefaultsender_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6uuq.htm
ms.date: 12/05/2018
ms.keywords: IFaxSender interface [Fax Service],SaveDefaultSender method, IFaxSender.SaveDefaultSender, IFaxSender::SaveDefaultSender, SaveDefaultSender, SaveDefaultSender method [Fax Service], SaveDefaultSender method [Fax Service],IFaxSender interface, _mfax_faxsender.savedefaultsender, fax._mfax_faxsender_cpp_mfax_faxsender_savedefaultsender_cpp, fax._mfax_faxsender_savedefaultsender, faxcomex/IFaxSender::SaveDefaultSender
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
 - IFaxSender::SaveDefaultSender
 - faxcomex/IFaxSender::SaveDefaultSender
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
 - IFaxSender.SaveDefaultSender
 - IFaxSender.SaveDefaultSender
---

# IFaxSender::SaveDefaultSender


## -description

The <b>IFaxSender::SaveDefaultSender</b> method stores information about the default sender from the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsender">FaxSender</a> object.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To load the default sender information into a <a href="/previous-versions/windows/desktop/fax/-mfax-faxsender">FaxSender</a> object, use the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsender-loaddefaultsender-vb">IFaxSender::get_LoadDefaultSender</a> method.

This method can return remote procedure call (RPC) return values. For more information, see <a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxsender">FaxSender</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxsender">IFaxSender</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-sending-a-fax">Visual Basic Example</a>
