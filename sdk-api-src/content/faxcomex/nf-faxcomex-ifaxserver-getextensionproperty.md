---
UID: NF:faxcomex.IFaxServer.GetExtensionProperty
title: IFaxServer::GetExtensionProperty (faxcomex.h)
author: windows-sdk-content
description: The IFaxServer::GetExtensionProperty method retrieves an extension configuration property stored at the server level.
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_getextensionproperty_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_1s3d.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetExtensionProperty, GetExtensionProperty method [Fax Service], GetExtensionProperty method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],GetExtensionProperty method, IFaxServer.GetExtensionProperty, IFaxServer::GetExtensionProperty, _mfax_faxserver.getextensionproperty, fax._mfax_faxserver_cpp_mfax_faxserver_getextensionproperty_cpp, fax._mfax_faxserver_getextensionproperty, faxcomex/IFaxServer::GetExtensionProperty
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxServer::GetExtensionProperty


## -description


The <b>IFaxServer::GetExtensionProperty</b> method retrieves an extension configuration property stored at the server level.


## -parameters




### -param bstrGUID [in]

Type: <b>BSTR</b>

Specifies a string GUID that uniquely identifies the data to be retrieved.


### -param pvProperty

TBD




#### - vProperty [out]

Type: <b>VARIANT*</b>

Pointer to a variable that receives a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> that specifies the data.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The returned data is a blob of bytes represented as a variant safe array of unsigned chars (VT_UI1 | VT_ARRAY). The data is only relevant to the specific extension that uses it. For more information see <a href="https://msdn.microsoft.com/en-us/library/ms684522(v=VS.85).aspx">About the Fax Extension Configuration API</a>.

To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms689109(v=VS.85).aspx">FaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689110(v=VS.85).aspx">IFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693437(v=VS.85).aspx">Visual Basic Example</a>
 

 

