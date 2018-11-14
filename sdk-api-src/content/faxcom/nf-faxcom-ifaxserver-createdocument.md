---
UID: NF:faxcom.IFaxServer.CreateDocument
title: IFaxServer::CreateDocument
author: windows-sdk-content
description: The IFaxServer::CreateDocument method creates a FaxDoc object for a specified FaxServer object. The FaxDoc object allows a user to create and transmit a document to one or more fax recipients.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_createdocument_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0cfo.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CreateDocument, CreateDocument method [Fax Service], CreateDocument method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],CreateDocument method, IFaxServer.CreateDocument, IFaxServer::CreateDocument, _mfax_ifaxserver_createdocument, fax._mfax_ifaxserver_client_mfax_ifaxserver_createdocument_cpp, fax._mfax_ifaxserver_createdocument, faxcom/IFaxServer::CreateDocument
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
 - IFaxServer.CreateDocument
 - IFaxServer.CreateDocument
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcom.h
: 
- IFaxServer.CreateDocument
: 
---

# IFaxServer::CreateDocument


## -description


The <b>IFaxServer::CreateDocument</b> method creates a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object for a specified <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The FaxDoc object allows a user to create and transmit a document to one or more fax recipients.


## -parameters




### -param FileName [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the fully qualified path and name of the file that contains the fax document to transmit. The path can be a UNC path or a path beginning with a drive letter.

This parameter can contain any valid local or remote file name. The file must be a properly registered file type, and the fax server must be able to access the file. 




### -param retval

TBD




#### - retVal [out]

Type: <b>VARIANT*</b>

Pointer to a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure that receives an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The method returns a pdispVal member with a VT_DISPATCH data type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>IFaxServer::CreateDocument</b> method retrieves an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. A fax client application can also access the <a href="https://msdn.microsoft.com/16f68004-fa4d-40c7-90a5-0bb562e72bd7">IFaxDoc</a> interface directly by calling the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an interface pointer. The <b>IFaxDoc</b> interface allows a user to set the properties for a fax document, and then transmit the document.

A fax client application should not call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve an <a href="https://msdn.microsoft.com/16f68004-fa4d-40c7-90a5-0bb562e72bd7">IFaxDoc</a> interface pointer because it will not be instantiated correctly.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a>



<a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a>



<a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a>



<a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a>
 

 

