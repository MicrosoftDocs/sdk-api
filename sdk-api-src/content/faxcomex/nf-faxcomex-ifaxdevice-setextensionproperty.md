---
UID: NF:faxcomex.IFaxDevice.SetExtensionProperty
title: IFaxDevice::SetExtensionProperty (faxcomex.h)
description: The IFaxDevice::SetExtensionProperty method stores an extension configuration property at the device level.
helpviewer_keywords: ["IFaxDevice interface [Fax Service]","SetExtensionProperty method","IFaxDevice.SetExtensionProperty","IFaxDevice::SetExtensionProperty","SetExtensionProperty","SetExtensionProperty method [Fax Service]","SetExtensionProperty method [Fax Service]","IFaxDevice interface","_mfax_faxdevice.setextensionproperty","fax._mfax_faxdevice_cpp_mfax_faxdevice_setextensionproperty_cpp","fax._mfax_faxdevice_setextensionproperty","faxcomex/IFaxDevice::SetExtensionProperty"]
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_setextensionproperty_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5szd.htm
ms.date: 12/05/2018
ms.keywords: IFaxDevice interface [Fax Service],SetExtensionProperty method, IFaxDevice.SetExtensionProperty, IFaxDevice::SetExtensionProperty, SetExtensionProperty, SetExtensionProperty method [Fax Service], SetExtensionProperty method [Fax Service],IFaxDevice interface, _mfax_faxdevice.setextensionproperty, fax._mfax_faxdevice_cpp_mfax_faxdevice_setextensionproperty_cpp, fax._mfax_faxdevice_setextensionproperty, faxcomex/IFaxDevice::SetExtensionProperty
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
 - IFaxDevice::SetExtensionProperty
 - faxcomex/IFaxDevice::SetExtensionProperty
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
 - IFaxDevice.SetExtensionProperty
 - IFaxDevice.SetExtensionProperty
---

# IFaxDevice::SetExtensionProperty


## -description

The <b>IFaxDevice::SetExtensionProperty</b> method stores an extension configuration property at the device level.

## -parameters

### -param bstrGUID [in]

Type: <b>BSTR</b>

Specifies a string GUID that identifies the data to set.

### -param vProperty [in]

Type: <b>VARIANT</b>

<b>VARIANT</b> that specifies the data to be stored.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> access right.

<div class="alert"><b>Note</b>  The required data is a blob of bytes represented as a variant safe array of unsigned chars (VT_UI1 | VT_ARRAY). The data is relevant only to the specific extension that uses it. For more information see <a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-extension-configuration-api">About the Fax Extension Configuration API</a>.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevice">IFaxDevice</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-extension-configuration-properties">Visual Basic Example</a>