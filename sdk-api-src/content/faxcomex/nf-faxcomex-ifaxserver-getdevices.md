---
UID: NF:faxcomex.IFaxServer.GetDevices
title: IFaxServer::GetDevices
author: windows-sdk-content
description: The IFaxServer::GetDevices method creates a IFaxDevices interface, a collection of all the fax devices exposed by all the fax service providers (FSPs) currently registered with the fax service.
old-location: fax\_mfax_faxserver_getdevices_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7hrn_cpp.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: GetDevices, GetDevices method [Fax Service], GetDevices method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],GetDevices method, IFaxServer.GetDevices, IFaxServer::GetDevices, _mfax_faxserver.getdevices_cpp, fax._mfax_faxserver_getdevices_cpp, faxcomex/IFaxServer::GetDevices
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
 - IFaxServer.GetDevices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxServer.GetDevices
: 
---

# IFaxServer::GetDevices


## -description


The <b>IFaxServer::GetDevices</b> method creates a <a href="https://msdn.microsoft.com/025b7393-b693-4d75-973a-4a058059eb22">IFaxDevices</a> interface, a collection of all the fax devices exposed by all the fax service providers (FSPs) currently registered with the fax service.


## -parameters




### -param ppFaxDevices [out, retval]

Type: <b><a href="https://msdn.microsoft.com/025b7393-b693-4d75-973a-4a058059eb22">IFaxDevices</a>**</b>

An address of a pointer that receives a <a href="https://msdn.microsoft.com/025b7393-b693-4d75-973a-4a058059eb22">IFaxDevices</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use the <a href="https://msdn.microsoft.com/025b7393-b693-4d75-973a-4a058059eb22">IFaxDevices</a> interface to enumerate the fax devices associated with a connected fax server and to create <a href="https://msdn.microsoft.com/3f4f4e83-df62-43af-903c-0b816bade3b9">IFaxDevice</a> interfaces for them.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>



<a href="https://msdn.microsoft.com/64bdc08c-1902-448a-9eda-b557ab4bb095">Visual Basic Example</a>
 

 

