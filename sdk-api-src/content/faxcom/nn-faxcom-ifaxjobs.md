---
UID: NN:faxcom.IFaxJobs
title: IFaxJobs
author: windows-sdk-content
description: The IFaxJobs dual interface is used by a fax client application to access the FaxJob objects derived from a FaxServer object. The interface enumerates the fax jobs associated with a connected fax server.
old-location: fax\_mfax_ifaxjobs.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8bjn.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
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
tech.root: 
req.typenames: ShellWindowTypeConstants
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
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxJobs interface


## -description


The <b>IFaxJobs</b> dual interface is used by a fax client application to access the <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> objects derived from a <a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a> object. The interface enumerates the fax jobs associated with a connected fax server.

A <a href="https://msdn.microsoft.com/7a8ad6e7-8db6-49ba-98de-da583907a54e">FaxJobs</a> object is a collection of <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> objects.

The <b>IFaxJobs</b> interface includes methods that allow a fax client application to perform the following tasks. 
			<ul>
<li>Retrieve the number of fax jobs associated with a connected fax server.</li>
<li>Create and retrieve IFaxJob interface pointers for FaxJob objects.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxJobs</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxJobs</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/476d4381-30b4-4749-b1ea-fbd28ca8148d">get_Count</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/476d4381-30b4-4749-b1ea-fbd28ca8148d">IFaxJobs::get_Count</a> method returns the number of queued fax jobs associated with the connected fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1279c69b-42b0-4ce2-92e1-307d3d7999b4">get_Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/1279c69b-42b0-4ce2-92e1-307d3d7999b4">IFaxJobs::get_Item</a> method returns a new <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> object for a specified fax job. The object allows enumeration of the fax jobs associated with a connected fax server.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxJobs</b> interface to create and retrieve <a href="https://msdn.microsoft.com/48de5e31-0286-4b7a-a86b-46411bf0e9e8">IFaxJob</a> interface pointers to <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> objects. There is one FaxJob object for each queued job associated with the connected fax server. 

To create an instance of a <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> object, perform the following steps. Note that a fax client application should not call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve an <a href="https://msdn.microsoft.com/48de5e31-0286-4b7a-a86b-46411bf0e9e8">IFaxJob</a> interface pointer. 
				<ol>
<li>Call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve a pointer to an IFaxServer interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">IFaxServer::Connect</a> method to connect to a fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/45b195f9-0ac9-4150-84cf-64049cc4053f">IFaxServer::GetJobs</a> method to create and initialize a <a href="https://msdn.microsoft.com/7a8ad6e7-8db6-49ba-98de-da583907a54e">FaxJobs</a> object for the fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/476d4381-30b4-4749-b1ea-fbd28ca8148d">IFaxJobs::get_Count</a> method and then the <a href="https://msdn.microsoft.com/1279c69b-42b0-4ce2-92e1-307d3d7999b4">IFaxJobs::get_Item</a> method to retrieve <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointers for each child <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> object.</li>
<li>Use the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to call <a href="https://msdn.microsoft.com/48de5e31-0286-4b7a-a86b-46411bf0e9e8">IFaxJob</a> interface methods. (You can also call the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxJob</b> interface pointer.)</li>
<li>Call the <a href="https://msdn.microsoft.com/dccbb6b1-b889-4b73-a3d0-9c5ce6268f4a">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="_com_IUnknown_Release">IUnknown::Release</a> method for each <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> object to allow the object to deallocate itself, and again to destroy the <b>IFaxJobs</b> interface pointer.</li>
</ol>





## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

