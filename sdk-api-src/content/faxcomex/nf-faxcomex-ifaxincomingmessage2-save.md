---
UID: NF:faxcomex.IFaxIncomingMessage2.Save
title: IFaxIncomingMessage2::Save (faxcomex.h)
description: Saves the FaxIncomingMessage object's data.helpviewer_keywords: ["IFaxIncomingMessage2 interface [Fax Service]","Save method","IFaxIncomingMessage2.Save","IFaxIncomingMessage2::Save","Save","Save method [Fax Service]","Save method [Fax Service]","IFaxIncomingMessage2 interface","_mfax_faxincomingmessage.save","fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_save_cpp","fax._mfax_faxincomingmessage_save","faxcomex/IFaxIncomingMessage2::Save"]
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_save_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\save.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],Save method, IFaxIncomingMessage2.Save, IFaxIncomingMessage2::Save, Save, Save method [Fax Service], Save method [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.save, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_save_cpp, fax._mfax_faxincomingmessage_save, faxcomex/IFaxIncomingMessage2::Save
f1_keywords:
- faxcomex/IFaxIncomingMessage2.Save
dev_langs:
- c++
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Fxscomex.dll
api_name:
- IFaxIncomingMessage2.Save
- IFaxIncomingMessage2.Save
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxIncomingMessage2::Save


## -description


Saves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a> object's data.


<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div><div> </div>

## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2MANAGE_CONFIG</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2QUERY_CONFIG</a> access rights.

It is not necessary to call this method to commit changes to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-subject-vb">IFaxIncomingMessage2::Subject</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-sendername-vb">IFaxIncomingMessage2::SenderName</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-senderfaxnumber-vb">IFaxIncomingMessage2::SenderFaxNumber</a>, and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-hascoverpage-vb">IFaxIncomingMessage2::HasCoverPage</a> properties. They are committed with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-reassign-vb">IFaxIncomingMessage2::Reassign</a> method.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage">IFaxIncomingMessage</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessage2">IFaxIncomingMessage2</a>
 

 

