---
UID: NF:faxcom.IFaxServer.GetJobs
title: IFaxServer::GetJobs
author: windows-sdk-content
description: The GetJobs method creates and initializes a FaxJobs object for a specified FaxServer object. The FaxJobs object allows enumeration of the current queued jobs for the connected fax server.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_getjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9uk3.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetJobs, GetJobs method [Fax Service], GetJobs method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],GetJobs method, IFaxServer.GetJobs, IFaxServer::GetJobs, _mfax_ifaxserver_getjobs, fax._mfax_ifaxserver_client_mfax_ifaxserver_getjobs_cpp, fax._mfax_ifaxserver_getjobs, faxcom/IFaxServer::GetJobs
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
 - IFaxServer.GetJobs
 - IFaxServer.GetJobs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxServer::GetJobs


## -description


The <b>GetJobs</b> method creates and initializes a <a href="https://msdn.microsoft.com/9df2f27f-b0a6-4ba5-920b-320dd83f6e40">FaxJobs</a> object for a specified <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <a href="https://msdn.microsoft.com/7a8ad6e7-8db6-49ba-98de-da583907a54e">FaxJobs</a> object allows enumeration of the current queued jobs for the connected fax server.


## -parameters




### -param retval

TBD




#### - retVal [out]

Type: <b>VARIANT*</b>

Pointer to a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure that receives an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/7a8ad6e7-8db6-49ba-98de-da583907a54e">FaxJobs</a> object. The method returns a pdispVal member with a VT_DISPATCH data type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>IFaxServer::GetJobs</b> method retrieves an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/7a8ad6e7-8db6-49ba-98de-da583907a54e">FaxJobs</a> object. A fax client application can also access the <a href="https://msdn.microsoft.com/c9e548c4-9381-4b7d-9a9d-55fbc59f198f">IFaxJobs</a> interface directly by calling the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an interface pointer.

A fax client application should not call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve an <a href="https://msdn.microsoft.com/c9e548c4-9381-4b7d-9a9d-55fbc59f198f">IFaxJobs</a> interface pointer because it will not be instantiated correctly.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a>



<a href="https://msdn.microsoft.com/48de5e31-0286-4b7a-a86b-46411bf0e9e8">IFaxJob</a>



<a href="https://msdn.microsoft.com/c9e548c4-9381-4b7d-9a9d-55fbc59f198f">IFaxJobs</a>



<a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a>



<a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a>
 

 

