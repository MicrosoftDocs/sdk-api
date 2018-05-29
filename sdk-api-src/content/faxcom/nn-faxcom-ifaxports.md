---
UID: NN:faxcom.IFaxPorts
title: IFaxPorts
author: windows-sdk-content
description: The IFaxPorts dual interface is used by a fax client application to access the FaxPort objects derived from a FaxServer object. The interface enumerates port configuration information for a connection to an active fax server.
old-location: fax\_mfax_ifaxports.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1hwz.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFaxPorts, IFaxPorts interface [Fax Service], IFaxPorts interface [Fax Service],described, _mfax_ifaxports, fax._mfax_ifaxports, faxcom/IFaxPorts
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
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Faxcom.dll
api_name:
-	IFaxPorts
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxPorts interface


## -description


The <b>IFaxPorts</b> dual interface is used by a fax client application to access the <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> objects derived from a <a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a> object. The interface enumerates port configuration information for a connection to an active fax server. A <a href="https://msdn.microsoft.com/ac1e4c87-ba3b-4b49-887c-ed392ddab455">FaxPorts</a> object is a collection of <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> objects. 

The <b>IFaxPorts</b> interface includes methods that allow a fax client application to perform the following tasks. 
			<ul>
<li>Retrieve the number of fax ports associated with a fax server.</li>
<li>Create and retrieve <a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a> interface pointers for <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> objects.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxPorts</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxPorts</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFaxPorts</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57736284-43f4-4ac3-bb43-313e6ee4ea44">get_Count</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/57736284-43f4-4ac3-bb43-313e6ee4ea44">IFaxPorts::get_Count</a> method retrieves the number of fax ports attached to the connected fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5819801-f213-42c9-b8d8-5eaf352c0361">get_Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c5819801-f213-42c9-b8d8-5eaf352c0361">IFaxPorts::get_Item</a> method creates a <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object for a specified fax port. The object allows enumeration of port configuration information for a specific connection to a fax server.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxPorts</b> interface to create and retrieve <a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a> interface pointers to <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> objects. There is one FaxPort object for each port associated with the connected fax server. 

To create an instance of a <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object, perform the following steps. Note that a fax client application should not call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve an <a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a> interface pointer. 
				<ol>
<li>Call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">IFaxServer::Connect</a> method to connect to an active fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/e10c4f3e-c8bd-4134-a325-fe7da93b1caa">IFaxServer::GetPorts</a> method to create and initialize a <a href="https://msdn.microsoft.com/ac1e4c87-ba3b-4b49-887c-ed392ddab455">FaxPorts</a> object for the connected fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/57736284-43f4-4ac3-bb43-313e6ee4ea44">IFaxPorts::get_Count</a> method and then the <a href="https://msdn.microsoft.com/c5819801-f213-42c9-b8d8-5eaf352c0361">IFaxPorts::get_Item</a> method to retrieve <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointers for each child <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. (You can also call the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an <a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a> interface pointer.)</li>
<li>Use the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to call <a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a> interface methods.</li>
<li>Call the <a href="https://msdn.microsoft.com/dccbb6b1-b889-4b73-a3d0-9c5ce6268f4a">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="_com_IUnknown_Release">IUnknown::Release</a> method for each <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object to allow the object to deallocate itself, and again to destroy the <b>IFaxPorts</b> interface pointer.</li>
</ol>





## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

