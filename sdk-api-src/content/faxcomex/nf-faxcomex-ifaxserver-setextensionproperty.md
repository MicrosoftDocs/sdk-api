---
UID: NF:faxcomex.IFaxServer.SetExtensionProperty
title: IFaxServer::SetExtensionProperty
author: windows-sdk-content
description: The IFaxServer::SetExtensionProperty method stores an extension configuration property at the server level.
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_setextensionproperty_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8gop.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxServer interface [Fax Service],SetExtensionProperty method, IFaxServer.SetExtensionProperty, IFaxServer::SetExtensionProperty, SetExtensionProperty, SetExtensionProperty method [Fax Service], SetExtensionProperty method [Fax Service],IFaxServer interface, _mfax_faxserver.setextensionproperty, fax._mfax_faxserver_cpp_mfax_faxserver_setextensionproperty_cpp, fax._mfax_faxserver_setextensionproperty, faxcomex/IFaxServer::SetExtensionProperty
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
 - IFaxServer.SetExtensionProperty
 - IFaxServer.SetExtensionProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


<a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> that specifies the data to be set.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The extension configuration property is a blob of bytes represented as a variant safe array of unsigned chars (VT_UI1 | VT_ARRAY). The data is only relevant to the specific extension that uses it. For more information see <a href="https://msdn.microsoft.com/846f307f-f2ec-4edd-8ada-cb2199dcfed5">About the Fax Extension Configuration API</a>.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>



<a href="https://msdn.microsoft.com/e9800209-9ff9-495d-ab60-a0cee64eb569">Visual Basic Example</a>
 

 

