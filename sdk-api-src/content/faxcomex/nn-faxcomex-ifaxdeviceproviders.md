---
UID: NN:faxcomex.IFaxDeviceProviders
title: IFaxDeviceProviders
author: windows-sdk-content
description: The IFaxDeviceProviders interface defines a configuration collection which contains the fax device providers on a connected fax server.
old-location: fax\_mfax_faxdeviceproviders_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_7vxv_cpp.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFaxDeviceProviders, IFaxDeviceProviders interface [Fax Service], IFaxDeviceProviders interface [Fax Service],described, _mfax_faxdeviceproviders_cpp, fax._mfax_faxdeviceproviders_cpp, faxcomex/IFaxDeviceProviders
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxDeviceProviders
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDeviceProviders interface


## -description


The <b>IFaxDeviceProviders</b> interface defines a configuration collection which contains the fax device providers on a connected fax server. This collection is used by a fax client application to retrieve information about the fax service providers (FSPs) registered with the fax service, represented by <a href="https://msdn.microsoft.com/ef32eb3d-e158-4740-82f5-661d5eded88c">FaxDeviceProvider</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDeviceProviders</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxDeviceProviders</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxDeviceProviders</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0a7986b-228a-471c-9fe4-cf23adafda10">get__NewEnum</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f0a7986b-228a-471c-9fe4-cf23adafda10">IFaxDeviceProviders::get__NewEnum</a> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/3abb80d7-fedf-469d-b17a-604ca78f4b8b">FaxDeviceProviders</a> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f1ab269-7186-4d86-936e-de0a238c0aab">get_Item</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/3f1ab269-7186-4d86-936e-de0a238c0aab">IFaxDeviceProviders::get_Item</a> property returns a <a href="https://msdn.microsoft.com/ef32eb3d-e158-4740-82f5-661d5eded88c">FaxDeviceProvider</a> object from the <a href="https://msdn.microsoft.com/3abb80d7-fedf-469d-b17a-604ca78f4b8b">FaxDeviceProviders</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDeviceProviders</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The Count property represents the number of objects in the FaxDeviceProviders collection. This is the total number of fax device providers associated with the fax server.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxDeviceProviders</b> is provided as the <a href="https://msdn.microsoft.com/3abb80d7-fedf-469d-b17a-604ca78f4b8b">FaxDeviceProviders</a> object.



