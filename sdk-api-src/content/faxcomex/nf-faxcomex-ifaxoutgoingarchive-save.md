---
UID: NF:faxcomex.IFaxOutgoingArchive.Save
title: IFaxOutgoingArchive::Save (faxcomex.h)
description: The IFaxOutgoingArchive::Save method saves the FaxOutgoingArchive object data.
helpviewer_keywords: ["IFaxOutgoingArchive interface [Fax Service]","Save method","IFaxOutgoingArchive.Save","IFaxOutgoingArchive::Save","Save","Save method [Fax Service]","Save method [Fax Service]","IFaxOutgoingArchive interface","_mfax_faxoutgoingarchive.save","fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_save_cpp","fax._mfax_faxoutgoingarchive_save","faxcomex/IFaxOutgoingArchive::Save"]
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_save_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_62ud.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingArchive interface [Fax Service],Save method, IFaxOutgoingArchive.Save, IFaxOutgoingArchive::Save, Save, Save method [Fax Service], Save method [Fax Service],IFaxOutgoingArchive interface, _mfax_faxoutgoingarchive.save, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_save_cpp, fax._mfax_faxoutgoingarchive_save, faxcomex/IFaxOutgoingArchive::Save
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
 - IFaxOutgoingArchive::Save
 - faxcomex/IFaxOutgoingArchive::Save
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
 - IFaxOutgoingArchive.Save
 - IFaxOutgoingArchive.Save
---

# IFaxOutgoingArchive::Save


## -description

The <b>IFaxOutgoingArchive::Save</b> method saves the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive">FaxOutgoingArchive</a> object data.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  In Windows Vista, Windows Server 2008, and later versions of Windows, this method is not supported and returns an error.</div>
<div> </div>
To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> and <b>farQUERY_CONFIG</b> access rights.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingarchive">FaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingarchive">IFaxOutgoingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-outgoing-archive">Visual Basic Example</a>
