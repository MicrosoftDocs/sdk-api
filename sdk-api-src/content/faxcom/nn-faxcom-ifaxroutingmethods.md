---
UID: NN:faxcom.IFaxRoutingMethods
title: IFaxRoutingMethods
author: windows-sdk-content
description: The IFaxRoutingMethods dual interface is used by a fax client application to access the FaxRoutingMethod objects derived from a FaxPort object.
old-location: fax\_mfax_ifaxroutingmethods.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6smr.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IFaxRoutingMethods, IFaxRoutingMethods interface [Fax Service], IFaxRoutingMethods interface [Fax Service],described, _mfax_ifaxroutingmethods, fax._mfax_ifaxroutingmethods, faxcom/IFaxRoutingMethods
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
 - IFaxRoutingMethods
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxRoutingMethods interface


## -description


The <b>IFaxRoutingMethods</b> dual interface is used by a fax client application to access the <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> objects derived from a <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The interface enumerates fax routing information for a specific fax port.  

A <a href="https://msdn.microsoft.com/8f164bc0-647c-4495-be67-2f208770c28d">FaxRoutingMethods</a> object is a collection of <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> objects. 

The <b>IFaxRoutingMethods</b> interface includes methods that allow a fax client application to perform the following tasks. 
			<ul>
<li>Retrieve the number of fax routing methods associated with a fax port.</li>
<li>Create and retrieve <a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a> interface pointers for <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> objects.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxRoutingMethods</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxRoutingMethods</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFaxRoutingMethods</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bbcf3aa-7dba-4452-817c-bf21bc646790">get_Count</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/7bbcf3aa-7dba-4452-817c-bf21bc646790">IFaxRoutingMethods::get_Count</a> returns the number of fax routing methods associated with a <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/403ba8dc-6faa-4067-b77a-9c451baa8a33">get_Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/403ba8dc-6faa-4067-b77a-9c451baa8a33">IFaxRoutingMethods::get_Item</a> method creates a <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> object for a specified fax routing method. The object allows enumeration of fax routing information for a specified <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxRoutingMethods</b> interface to create and retrieve <a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a> interface pointers to <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> objects. There is one FaxRoutingMethod object for each routing method associated with the specified fax port.  

To create an instance of a <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> object, perform the following steps. Note that a fax client application should not call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve an <a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a> interface pointer.  
				<ol>
<li>Call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">IFaxServer::Connect</a> method to connect to a fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/c180dbac-2aaa-4e8e-9b1f-b6314b47d229">IFaxPort::GetRoutingMethods</a> method to create and initialize a <a href="https://msdn.microsoft.com/8f164bc0-647c-4495-be67-2f208770c28d">FaxRoutingMethods</a> object for the fax port.</li>
<li>Call the <a href="https://msdn.microsoft.com/7bbcf3aa-7dba-4452-817c-bf21bc646790">IFaxRoutingMethods::get_Count</a> method and then the <a href="https://msdn.microsoft.com/403ba8dc-6faa-4067-b77a-9c451baa8a33">IFaxRoutingMethods::get_Item</a> method to retrieve <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointers for each child <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> object. (You can also call the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an <a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a> interface pointer). </li>
<li>Use the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to call <a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a> interface methods.</li>
<li>Call the <a href="https://msdn.microsoft.com/dccbb6b1-b889-4b73-a3d0-9c5ce6268f4a">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="_com_IUnknown_Release">IUnknown::Release</a> method for each <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> object to allow the object to deallocate itself, and again to destroy the <b>IFaxRoutingMethods</b> interface pointer.</li>
</ol>





## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

