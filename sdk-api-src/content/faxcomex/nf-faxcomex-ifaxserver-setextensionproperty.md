---
UID: NF:faxcomex.IFaxServer.SetExtensionProperty
title: IFaxServer::SetExtensionProperty (faxcomex.h)
description: The IFaxServer::SetExtensionProperty method stores an extension configuration property at the server level.
helpviewer_keywords: ["IFaxServer interface [Fax Service]","SetExtensionProperty method","IFaxServer.SetExtensionProperty","IFaxServer::SetExtensionProperty","SetExtensionProperty","SetExtensionProperty method [Fax Service]","SetExtensionProperty method [Fax Service]","IFaxServer interface","_mfax_faxserver.setextensionproperty","fax._mfax_faxserver_cpp_mfax_faxserver_setextensionproperty_cpp","fax._mfax_faxserver_setextensionproperty","faxcomex/IFaxServer::SetExtensionProperty"]
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_setextensionproperty_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8gop.htm
ms.date: 12/05/2018
ms.keywords: IFaxServer interface [Fax Service],SetExtensionProperty method, IFaxServer.SetExtensionProperty, IFaxServer::SetExtensionProperty, SetExtensionProperty, SetExtensionProperty method [Fax Service], SetExtensionProperty method [Fax Service],IFaxServer interface, _mfax_faxserver.setextensionproperty, fax._mfax_faxserver_cpp_mfax_faxserver_setextensionproperty_cpp, fax._mfax_faxserver_setextensionproperty, faxcomex/IFaxServer::SetExtensionProperty
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
 - IFaxServer::SetExtensionProperty
 - faxcomex/IFaxServer::SetExtensionProperty
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
 - IFaxServer.SetExtensionProperty
 - IFaxServer.SetExtensionProperty
---

# IFaxServer::SetExtensionProperty


## -description

The <b>IFaxServer::SetExtensionProperty</b> method stores an extension configuration property at the server level.

## -parameters

### -param bstrGUID [in]

Type: <b>BSTR</b>

Specifies a string GUID that identifies the data to set.

### -param vProperty [in]

Type: <b>VARIANT</b>


<a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> that specifies the data to be set.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The extension configuration property is a blob of bytes represented as a variant safe array of unsigned chars (VT_UI1 | VT_ARRAY). The data is only relevant to the specific extension that uses it. For more information see <a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-extension-configuration-api">About the Fax Extension Configuration API</a>.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-extension-configuration-properties">Visual Basic Example</a>