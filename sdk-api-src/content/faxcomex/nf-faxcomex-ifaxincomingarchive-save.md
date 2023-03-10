---
UID: NF:faxcomex.IFaxIncomingArchive.Save
title: IFaxIncomingArchive::Save (faxcomex.h)
description: The Save method saves the FaxIncomingArchive object's data.
helpviewer_keywords: ["IFaxIncomingArchive interface [Fax Service]","Save method","IFaxIncomingArchive.Save","IFaxIncomingArchive::Save","Save","Save method [Fax Service]","Save method [Fax Service]","IFaxIncomingArchive interface","_mfax_faxincomingarchive.save","fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_save_cpp","fax._mfax_faxincomingarchive_save","faxcomex/IFaxIncomingArchive::Save"]
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_save_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_8jfp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingArchive interface [Fax Service],Save method, IFaxIncomingArchive.Save, IFaxIncomingArchive::Save, Save, Save method [Fax Service], Save method [Fax Service],IFaxIncomingArchive interface, _mfax_faxincomingarchive.save, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_save_cpp, fax._mfax_faxincomingarchive_save, faxcomex/IFaxIncomingArchive::Save
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
 - IFaxIncomingArchive::Save
 - faxcomex/IFaxIncomingArchive::Save
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
 - IFaxIncomingArchive.Save
 - IFaxIncomingArchive.Save
---

# IFaxIncomingArchive::Save


## -description

The <b>Save</b> method saves the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a> object's data.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  In Windows Vista, Windows Server 2008, and later versions of Windows, this method is not supported and returns an error.</div>
<div> </div>
To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> and <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access rights.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive">FaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-opening-a-fax-from-the-incoming-archive">Visual Basic Example</a>
