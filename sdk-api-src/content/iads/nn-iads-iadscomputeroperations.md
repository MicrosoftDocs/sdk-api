---
UID: NN:iads.IADsComputerOperations
title: IADsComputerOperations
author: windows-sdk-content
description: The IADsComputerOperations interface is a dual interface that inherits from IADs.
old-location: adsi\iadscomputeroperations.htm
old-project: ADSI
ms.assetid: 9b0155ce-f313-43fa-8605-650aa8f38587
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IADsComputerOperations, IADsComputerOperations interface [ADSI], IADsComputerOperations interface [ADSI],described, _ds_iadscomputeroperations, adsi.iadscomputeroperations, iads/IADsComputerOperations
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Activeds.dll
api_name:
-	IADsComputerOperations
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsComputerOperations interface


## -description


The <b>IADsComputerOperations</b> interface is a dual interface that inherits from  <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>. It exposes methods for retrieving the status of a computer over a network and to enable remote shutdown. Directory service providers may choose to implement this interface to support basic system administration over a network through ADSI.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsComputerOperations</b> interface inherits from <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> and <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>. <b>IADsComputerOperations</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsComputerOperations</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>
</td>
<td align="left" width="63%">
Gets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cda6b8e7-fadc-4e0b-8217-66b37bf7efbd">GetEx</a>
</td>
<td align="left" width="63%">
Gets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451309">GetInfo</a>
</td>
<td align="left" width="63%">
Loads the property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">GetInfoEx</a>
</td>
<td align="left" width="63%">
Loads specific property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">Put</a>
</td>
<td align="left" width="63%">
Sets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">PutEx</a>
</td>
<td align="left" width="63%">
Sets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">SetInfo</a>
</td>
<td align="left" width="63%">
Persists the changes on this object to the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a>
</td>
<td align="left" width="63%">
Executes shutdown with optional reboot.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>
</td>
<td align="left" width="63%">
Returns the current operations status.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsComputerOperations</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">AdsPath</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the object's ADsPath that uniquely identifies this object from all others.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Class</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the name of the object's schema class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the GUID of the object as stored in the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the object's relative name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Parent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ADsPath string for the parent of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Schema</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ADsPath string to the schema class object for this object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/e2b90a98-5777-42c2-95dd-4623e738c4da">IADsComputer</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

