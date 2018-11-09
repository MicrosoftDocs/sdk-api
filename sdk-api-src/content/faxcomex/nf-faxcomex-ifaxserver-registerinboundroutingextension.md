---
UID: NF:faxcomex.IFaxServer.RegisterInboundRoutingExtension
title: IFaxServer::RegisterInboundRoutingExtension
author: windows-sdk-content
description: The IFaxServer::RegisterInboundRoutingExtension method registers a fax inbound routing extension with the fax service. Registration takes place after the fax service restarts.
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_registerinboundroutingextension_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_9kfi.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxServer interface [Fax Service],RegisterInboundRoutingExtension method, IFaxServer.RegisterInboundRoutingExtension, IFaxServer::RegisterInboundRoutingExtension, RegisterInboundRoutingExtension, RegisterInboundRoutingExtension method [Fax Service], RegisterInboundRoutingExtension method [Fax Service],IFaxServer interface, _mfax_faxserver.registerinboundroutingextension, fax._mfax_faxserver_cpp_mfax_faxserver_registerinboundroutingextension_cpp, fax._mfax_faxserver_registerinboundroutingextension, faxcomex/IFaxServer::RegisterInboundRoutingExtension
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
 - IFaxServer.RegisterInboundRoutingExtension
 - IFaxServer.RegisterInboundRoutingExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxServer::RegisterInboundRoutingExtension


## -description


The <b>IFaxServer::RegisterInboundRoutingExtension</b> method registers a fax inbound routing extension with the fax service. Registration takes place after the fax service restarts.


## -parameters




### -param bstrExtensionName

Type: <b>BSTR</b>

String that specifies the internal name of the fax routing extension DLL.


### -param bstrFriendlyName

Type: <b>BSTR</b>

String to associate with the fax routing extension DLL. This is the routing extension's user-friendly name, suitable for display.


### -param bstrImageName

Type: <b>BSTR</b>

String that specifies the full path and file name for the fax routing extension DLL. The path can include valid environment variables, for example, %SYSTEMDRIVE% and %SYSTEMROOT%.


### -param vMethods

Type: <b>VARIANT</b>


<a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> that specifies a safearray of <b>BSTR</b>s. The array must be unidimensional, it cannot be empty, and it must have a lower limit of zero. Each item (string) in the array must identify a routing method. The string must have the following format: Method name; Friendly name; Function Name; Method GUID


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Only an administrator can register a routing extension. Also, this method works only on the local fax server.

This property is not supported in Windows XP, and will return the error: <a href="https://msdn.microsoft.com/b5d59fec-2802-40bd-8ce4-748137f30fb2">FAX_E_NOT_SUPPORTED_ON_THIS_SKU</a>. 

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>
 

 

