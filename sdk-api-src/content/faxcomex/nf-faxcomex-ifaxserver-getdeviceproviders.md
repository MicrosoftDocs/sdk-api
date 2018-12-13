---
UID: NF:faxcomex.IFaxServer.GetDeviceProviders
title: IFaxServer::GetDeviceProviders
author: windows-sdk-content
description: The IFaxServer::GetDeviceProviders method creates a IFaxDeviceProviders interface, a collection of fax service providers (FSPs) that are currently registered with the fax service.
old-location: fax\_mfax_faxserver_getdeviceproviders_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6xv7_cpp.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDeviceProviders, GetDeviceProviders method [Fax Service], GetDeviceProviders method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],GetDeviceProviders method, IFaxServer.GetDeviceProviders, IFaxServer::GetDeviceProviders, _mfax_faxserver.getdeviceproviders_cpp, fax._mfax_faxserver_getdeviceproviders_cpp, faxcomex/IFaxServer::GetDeviceProviders
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
 - IFaxServer.GetDeviceProviders
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxServer::GetDeviceProviders


## -description


The <b>IFaxServer::GetDeviceProviders</b> method creates a <a href="https://msdn.microsoft.com/en-us/library/ms687081(v=VS.85).aspx">IFaxDeviceProviders</a> interface, a collection of fax service providers (FSPs) that are currently registered with the fax service. You can use the <b>IFaxDeviceProviders</b> interface to enumerate the FSPs associated with a fax server and to create and access <a href="https://msdn.microsoft.com/en-us/library/ms684893(v=VS.85).aspx">IFaxDeviceProvider</a> interfaces for them.


## -parameters




### -param ppFaxDeviceProviders [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms687081(v=VS.85).aspx">IFaxDeviceProviders</a>**</b>

An address of a pointer that receives a <a href="https://msdn.microsoft.com/en-us/library/ms687081(v=VS.85).aspx">IFaxDeviceProviders</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms689109(v=VS.85).aspx">FaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689110(v=VS.85).aspx">IFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693462(v=VS.85).aspx">Visual Basic Example</a>
 

 

