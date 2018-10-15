---
UID: NF:faxcomex.IFaxServer.GetExtensionProperty
title: IFaxServer::GetExtensionProperty
author: windows-sdk-content
description: The IFaxServer::GetExtensionProperty method retrieves an extension configuration property stored at the server level.
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_getextensionproperty_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_1s3d.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetExtensionProperty, GetExtensionProperty method [Fax Service], GetExtensionProperty method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],GetExtensionProperty method, IFaxServer.GetExtensionProperty, IFaxServer::GetExtensionProperty, _mfax_faxserver.getextensionproperty, fax._mfax_faxserver_cpp_mfax_faxserver_getextensionproperty_cpp, fax._mfax_faxserver_getextensionproperty, faxcomex/IFaxServer::GetExtensionProperty
ms.prod: windows-hardware
ms.technology: windows-devices
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

Pointer to a variable that receives a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> that specifies the data.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The returned data is a blob of bytes represented as a variant safe array of unsigned chars (VT_UI1 | VT_ARRAY). The data is only relevant to the specific extension that uses it. For more information see <a href="https://msdn.microsoft.com/846f307f-f2ec-4edd-8ada-cb2199dcfed5">About the Fax Extension Configuration API</a>.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>



<a href="https://msdn.microsoft.com/e9800209-9ff9-495d-ab60-a0cee64eb569">Visual Basic Example</a>
 

 

