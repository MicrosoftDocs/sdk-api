---
UID: NF:faxcomex.IFaxSecurity.Save
title: IFaxSecurity::Save (faxcomex.h)
description: The IFaxSecurity::Save method saves the FaxSecurity object data.
helpviewer_keywords: ["IFaxSecurity interface [Fax Service]","Save method","IFaxSecurity.Save","IFaxSecurity::Save","Save","Save method [Fax Service]","Save method [Fax Service]","IFaxSecurity interface","_mfax_faxsecurity.save","fax._mfax_faxsecurity_cpp_mfax_faxsecurity_save_cpp","fax._mfax_faxsecurity_save","faxcomex/IFaxSecurity::Save"]
old-location: fax\_mfax_faxsecurity_cpp_mfax_faxsecurity_save_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_9qzp.htm
ms.date: 12/05/2018
ms.keywords: IFaxSecurity interface [Fax Service],Save method, IFaxSecurity.Save, IFaxSecurity::Save, Save, Save method [Fax Service], Save method [Fax Service],IFaxSecurity interface, _mfax_faxsecurity.save, fax._mfax_faxsecurity_cpp_mfax_faxsecurity_save_cpp, fax._mfax_faxsecurity_save, faxcomex/IFaxSecurity::Save
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
 - IFaxSecurity::Save
 - faxcomex/IFaxSecurity::Save
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
 - IFaxSecurity.Save
 - IFaxSecurity.Save
---

# IFaxSecurity::Save


## -description

The <b>IFaxSecurity::Save</b> method saves the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity">FaxSecurity</a> object data.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> and <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access rights.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity">FaxSecurity</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxsecurity">IFaxSecurity</a>
