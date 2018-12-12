---
UID: NF:faxcom.IFaxServer.put_Retries
title: IFaxServer::put_Retries
author: windows-sdk-content
description: Sets or retrieves the Retries property for a FaxServer object. The Retries property is a value that represents the number of times the fax server attempts to retransmit an outgoing fax when the initial transmission fails.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_retries_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3veb.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxServer interface [Fax Service],Retries property, IFaxServer.Retries, IFaxServer.get_Retries, IFaxServer.put_Retries, IFaxServer::Retries, IFaxServer::get_Retries, IFaxServer::put_Retries, Retries property [Fax Service], Retries property [Fax Service],IFaxServer interface, _mfax_ifaxserver_get_retries, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_retries_cpp, fax._mfax_ifaxserver_get_retries, faxcom/IFaxServer::Retries, faxcom/IFaxServer::get_Retries, faxcom/IFaxServer::put_Retries, put_Retries
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxServer.Retries
 - IFaxServer.get_Retries
 - IFaxServer.put_Retries
 - IFaxServer.get_Retries
 - IFaxServer.put_Retries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxServer::put_Retries


## -description


Sets or retrieves the <b>Retries</b> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>Retries</b> property is a value that represents the number of times the fax server attempts to retransmit an outgoing fax when the initial transmission fails.

This property is read/write.


## -parameters


## -remarks



A transmission might not be sent on the first attempt for various reasons. For example, the sending device may receive a busy signal. 




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a>



<a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a>
 

 

