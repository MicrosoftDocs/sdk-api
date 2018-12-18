---
UID: NF:faxcom.IFaxServer.GetPorts
title: IFaxServer::GetPorts
author: windows-sdk-content
description: The GetPorts method creates and initializes a FaxPorts object for a specified FaxServer object. The FaxPorts object allows enumeration of fax port configuration information for the connected fax server.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_getports_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9apf.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPorts, GetPorts method [Fax Service], GetPorts method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],GetPorts method, IFaxServer.GetPorts, IFaxServer::GetPorts, _mfax_ifaxserver_getports, fax._mfax_ifaxserver_client_mfax_ifaxserver_getports_cpp, fax._mfax_ifaxserver_getports, faxcom/IFaxServer::GetPorts
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
 - IFaxServer.GetPorts
 - IFaxServer.GetPorts
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxServer::GetPorts


## -description


The <b>GetPorts</b> method creates and initializes a <a href="https://msdn.microsoft.com/ac1e4c87-ba3b-4b49-887c-ed392ddab455">FaxPorts</a> object for a specified <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The FaxPorts object allows enumeration of fax port configuration information for the connected fax server.


## -parameters




### -param retval

TBD




#### - retVal [out]

Type: <b>VARIANT*</b>

Pointer to a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure that receives an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/74ccb74e-7eb9-4617-ae0b-01f6f2095801">FaxPorts</a> object. The method returns a pdispVal member with a VT_DISPATCH data type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>IFaxServer::GetPorts</b> method retrieves an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/ac1e4c87-ba3b-4b49-887c-ed392ddab455">FaxPorts</a> object. A fax client application can also access the <a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a> interface directly by calling the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an interface pointer.

A fax client application should not call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve an <a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a> interface pointer because it will not be instantiated correctly.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>



<a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a>



<a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a>
 

 

