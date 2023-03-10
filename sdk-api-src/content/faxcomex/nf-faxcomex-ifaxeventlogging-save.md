---
UID: NF:faxcomex.IFaxEventLogging.Save
title: IFaxEventLogging::Save (faxcomex.h)
description: The IFaxEventLogging::Save method saves the IFaxEventLogging interface's data.
helpviewer_keywords: ["IFaxEventLogging interface [Fax Service]","Save method","IFaxEventLogging.Save","IFaxEventLogging::Save","Save","Save method [Fax Service]","Save method [Fax Service]","IFaxEventLogging interface","_mfax_faxeventlogging.save","fax._mfax_faxeventlogging_cpp_mfax_faxeventlogging_save_cpp","fax._mfax_faxeventlogging_save","faxcomex/IFaxEventLogging::Save"]
old-location: fax\_mfax_faxeventlogging_cpp_mfax_faxeventlogging_save_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_16cl.htm
ms.date: 12/05/2018
ms.keywords: IFaxEventLogging interface [Fax Service],Save method, IFaxEventLogging.Save, IFaxEventLogging::Save, Save, Save method [Fax Service], Save method [Fax Service],IFaxEventLogging interface, _mfax_faxeventlogging.save, fax._mfax_faxeventlogging_cpp_mfax_faxeventlogging_save_cpp, fax._mfax_faxeventlogging_save, faxcomex/IFaxEventLogging::Save
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
 - IFaxEventLogging::Save
 - faxcomex/IFaxEventLogging::Save
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
 - IFaxEventLogging.Save
 - IFaxEventLogging.Save
---

# IFaxEventLogging::Save


## -description

The <b>IFaxEventLogging::Save</b> method saves the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxeventlogging">IFaxEventLogging</a> interface's data.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> and <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access rights.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceprovider">FaxDeviceProvider</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceprovider">IFaxDeviceProvider</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxeventlogging">IFaxEventLogging</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-logging-options">Visual Basic Example</a>
