---
UID: NN:faxcom.IFaxJobs
title: IFaxJobs
author: windows-sdk-content
description: The IFaxJobs dual interface is used by a fax client application to access the FaxJob objects derived from a FaxServer object. The interface enumerates the fax jobs associated with a connected fax server.
old-location: fax\_mfax_ifaxjobs.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8bjn.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxJobs, IFaxJobs interface [Fax Service], IFaxJobs interface [Fax Service],described, _mfax_ifaxjobs, fax._mfax_ifaxjobs, faxcom/IFaxJobs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IFaxJobs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxJobs interface


## -description


The <b>IFaxJobs</b> dual interface is used by a fax client application to access the <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> objects derived from a <a href="https://msdn.microsoft.com/en-us/library/ms689109(v=VS.85).aspx">FaxServer</a> object. The interface enumerates the fax jobs associated with a connected fax server.

A <a href="https://msdn.microsoft.com/en-us/library/ms692796(v=VS.85).aspx">FaxJobs</a> object is a collection of <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> objects.

The <b>IFaxJobs</b> interface includes methods that allow a fax client application to perform the following tasks. 
			<ul>
<li>Retrieve the number of fax jobs associated with a connected fax server.</li>
<li>Create and retrieve IFaxJob interface pointers for FaxJob objects.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxJobs</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxJobs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFaxJobs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms691382(v=VS.85).aspx">get_Count</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms691382(v=VS.85).aspx">IFaxJobs::get_Count</a> method returns the number of queued fax jobs associated with the connected fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms691271(v=VS.85).aspx">get_Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms691271(v=VS.85).aspx">IFaxJobs::get_Item</a> method returns a new <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> object for a specified fax job. The object allows enumeration of the fax jobs associated with a connected fax server.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxJobs</b> interface to create and retrieve <a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a> interface pointers to <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> objects. There is one FaxJob object for each queued job associated with the connected fax server. 

To create an instance of a <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> object, perform the following steps. Note that a fax client application should not call the <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function to retrieve an <a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a> interface pointer. 
				<ol>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function to retrieve a pointer to an IFaxServer interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms692315(v=VS.85).aspx">IFaxServer::Connect</a> method to connect to a fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms692836(v=VS.85).aspx">IFaxServer::GetJobs</a> method to create and initialize a <a href="https://msdn.microsoft.com/en-us/library/ms692796(v=VS.85).aspx">FaxJobs</a> object for the fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms691382(v=VS.85).aspx">IFaxJobs::get_Count</a> method and then the <a href="https://msdn.microsoft.com/en-us/library/ms691271(v=VS.85).aspx">IFaxJobs::get_Item</a> method to retrieve <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointers for each child <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> object.</li>
<li>Use the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer to call <a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a> interface methods. (You can also call the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxJob</b> interface pointer.)</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms691936(v=VS.85).aspx">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method for each <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> object to allow the object to deallocate itself, and again to destroy the <b>IFaxJobs</b> interface pointer.</li>
</ol>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

