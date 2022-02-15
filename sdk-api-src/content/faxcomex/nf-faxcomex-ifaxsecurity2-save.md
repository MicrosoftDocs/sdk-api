---
UID: NF:faxcomex.IFaxSecurity2.Save
title: IFaxSecurity2::Save (faxcomex.h)
description: Saves the FaxSecurity object data.
helpviewer_keywords: ["IFaxSecurity2 interface [Fax Service]","Save method","IFaxSecurity2.Save","IFaxSecurity2::Save","Save","Save method [Fax Service]","Save method [Fax Service]","IFaxSecurity2 interface","_mfax_faxsecurity2.save","fax._mfax_faxsecurity2_cpp_mfax_faxsecurity2_save_cpp","fax._mfax_faxsecurity2_save","faxcomex/IFaxSecurity2::Save"]
old-location: fax\_mfax_faxsecurity2_cpp_mfax_faxsecurity2_save_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxsecurity2\save.htm
ms.date: 12/05/2018
ms.keywords: IFaxSecurity2 interface [Fax Service],Save method, IFaxSecurity2.Save, IFaxSecurity2::Save, Save, Save method [Fax Service], Save method [Fax Service],IFaxSecurity2 interface, _mfax_faxsecurity2.save, fax._mfax_faxsecurity2_cpp_mfax_faxsecurity2_save_cpp, fax._mfax_faxsecurity2_save, faxcomex/IFaxSecurity2::Save
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxSecurity2::Save
 - faxcomex/IFaxSecurity2::Save
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
 - IFaxSecurity2.Save
 - IFaxSecurity2.Save
---

# IFaxSecurity2::Save


## -description

Saves the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity">FaxSecurity</a> object data.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2MANAGE_CONFIG</a> and <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2QUERY_CONFIG</a> access rights.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2">FaxSecurity2</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxsecurity2">IFaxSecurity2</a>
