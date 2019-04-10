---
UID: NF:faxcom.IFaxServer.GetJobs
title: IFaxServer::GetJobs (faxcom.h)
author: windows-sdk-content
description: The GetJobs method creates and initializes a FaxJobs object for a specified FaxServer object. The FaxJobs object allows enumeration of the current queued jobs for the connected fax server.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_getjobs_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9uk3.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
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


The <b>GetJobs</b> method creates and initializes a <a href="https://msdn.microsoft.com/en-us/library/ms690701(v=VS.85).aspx">FaxJobs</a> object for a specified <a href="https://msdn.microsoft.com/en-us/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <a href="https://msdn.microsoft.com/en-us/library/ms692796(v=VS.85).aspx">FaxJobs</a> object allows enumeration of the current queued jobs for the connected fax server.


## -parameters




### -param retval

TBD




#### - retVal [out]

Type: <b>VARIANT*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure that receives an <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms692796(v=VS.85).aspx">FaxJobs</a> object. The method returns a pdispVal member with a VT_DISPATCH data type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>IFaxServer::GetJobs</b> method retrieves an <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms692796(v=VS.85).aspx">FaxJobs</a> object. A fax client application can also access the <a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a> interface directly by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method to retrieve an interface pointer.

A fax client application should not call the <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function to retrieve an <a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a> interface pointer because it will not be instantiated correctly.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692367(v=VS.85).aspx">FaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692375(v=VS.85).aspx">IFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a>
 

 

