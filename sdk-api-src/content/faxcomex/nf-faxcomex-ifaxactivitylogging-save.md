---
UID: NF:faxcomex.IFaxActivityLogging.Save
title: IFaxActivityLogging::Save (faxcomex.h)
description: The IFaxActivityLogging::Save method saves the FaxActivityLogging object's data.
helpviewer_keywords: ["IFaxActivityLogging interface [Fax Service]","Save method","IFaxActivityLogging.Save","IFaxActivityLogging::Save","Save","Save method [Fax Service]","Save method [Fax Service]","IFaxActivityLogging interface","_mfax_faxactivitylogging.save","fax._mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_save_cpp","fax._mfax_faxactivitylogging_save","faxcomex/IFaxActivityLogging::Save"]
old-location: fax\_mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_save_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_3ht1.htm
ms.date: 12/05/2018
ms.keywords: IFaxActivityLogging interface [Fax Service],Save method, IFaxActivityLogging.Save, IFaxActivityLogging::Save, Save, Save method [Fax Service], Save method [Fax Service],IFaxActivityLogging interface, _mfax_faxactivitylogging.save, fax._mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_save_cpp, fax._mfax_faxactivitylogging_save, faxcomex/IFaxActivityLogging::Save
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
 - IFaxActivityLogging::Save
 - faxcomex/IFaxActivityLogging::Save
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
 - IFaxActivityLogging.Save
 - IFaxActivityLogging.Save
---

# IFaxActivityLogging::Save


## -description

The <b>IFaxActivityLogging::Save</b> method saves the <a href="/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging">FaxActivityLogging</a> object's data.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> and <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> access rights.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging">FaxActivityLogging</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxactivitylogging">IFaxActivityLogging</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-logging-options">Visual Basic Example</a>
