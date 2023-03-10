---
UID: NF:faxcomex.IFaxServer.GetExtensionProperty
title: IFaxServer::GetExtensionProperty (faxcomex.h)
description: The IFaxServer::GetExtensionProperty method retrieves an extension configuration property stored at the server level.
helpviewer_keywords: ["GetExtensionProperty","GetExtensionProperty method [Fax Service]","GetExtensionProperty method [Fax Service]","IFaxServer interface","IFaxServer interface [Fax Service]","GetExtensionProperty method","IFaxServer.GetExtensionProperty","IFaxServer::GetExtensionProperty","_mfax_faxserver.getextensionproperty","fax._mfax_faxserver_cpp_mfax_faxserver_getextensionproperty_cpp","fax._mfax_faxserver_getextensionproperty","faxcomex/IFaxServer::GetExtensionProperty"]
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_getextensionproperty_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_1s3d.htm
ms.date: 12/05/2018
ms.keywords: GetExtensionProperty, GetExtensionProperty method [Fax Service], GetExtensionProperty method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],GetExtensionProperty method, IFaxServer.GetExtensionProperty, IFaxServer::GetExtensionProperty, _mfax_faxserver.getextensionproperty, fax._mfax_faxserver_cpp_mfax_faxserver_getextensionproperty_cpp, fax._mfax_faxserver_getextensionproperty, faxcomex/IFaxServer::GetExtensionProperty
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
 - IFaxServer::GetExtensionProperty
 - faxcomex/IFaxServer::GetExtensionProperty
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
 - IFaxServer.GetExtensionProperty
 - IFaxServer.GetExtensionProperty
---

## -description

The <b>IFaxServer::GetExtensionProperty</b> method retrieves an extension configuration property stored at the server level.

## -parameters

### -param bstrGUID

Type: [in] <b>BSTR</b>

Specifies a string GUID that uniquely identifies the data to be retrieved.

### -param pvProperty [out]

Type: <b>VARIANT*</b>

Pointer to a variable that receives a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> that specifies the data.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The returned data is a blob of bytes represented as a variant safe array of unsigned chars (VT_UI1 | VT_ARRAY). The data is only relevant to the specific extension that uses it. For more information see <a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-extension-configuration-api">About the Fax Extension Configuration API</a>.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-extension-configuration-properties">Visual Basic Example</a>