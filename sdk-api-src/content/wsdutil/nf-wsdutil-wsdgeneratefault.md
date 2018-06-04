---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WSDGenerateFault function


## -description


Generates a SOAP fault.


## -parameters




### -param pszCode [in]

A SOAP fault code.


The list of possible fault codes follows. For a description of each fault code, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=69438">SOAP Version 1.2 specification</a>.



<a id="VersionMismatch"></a>
<a id="versionmismatch"></a>
<a id="VERSIONMISMATCH"></a>


#### VersionMismatch

<a id="MustUnderstand"></a>
<a id="mustunderstand"></a>
<a id="MUSTUNDERSTAND"></a>


#### MustUnderstand

<a id="DataEncodingUnknown"></a>
<a id="dataencodingunknown"></a>
<a id="DATAENCODINGUNKNOWN"></a>


#### DataEncodingUnknown

<a id="Sender"></a>
<a id="sender"></a>
<a id="SENDER"></a>


#### Sender

<a id="Receiver"></a>
<a id="receiver"></a>
<a id="RECEIVER"></a>


#### Receiver


### -param pszSubCode [in]

A fault subcode.


### -param pszReason [in]

A human readable explanation of the fault.


### -param pszDetail [in]

Contains application-specific error information pertaining to the fault.


### -param pContext [in]

An <a href="https://msdn.microsoft.com/131fa170-4c19-4a7b-82e0-e9677b7f767a">IWSDXMLContext</a> interface that represents the context in which to generate the fault.


### -param ppFault [out]

A <a href="https://msdn.microsoft.com/ed5e2575-203a-41a2-b656-50cb82aae088">WSD_SOAP_FAULT</a> structure that contains the generated fault.  When the calling application is done with this data, <i>ppFault</i> must be freed with a call to <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a>.


## -returns



Possible return values include, but are not limited to, the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pszCode</i>, <i>pszReason</i>, or <i>pContext</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppFault</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



SOAP faults provide a way to communicate error information on failed SOAP messages. Different Web Services protocols extend faults to provide contextual error information, and in some cases, like in WS-Eventing, faults are an expected part of specific message patterns as the client determines whether or not the device supports specific features.

The following fault subcodes are not implemented by WSDAPI:<ul>
<li>InvalidMessageInformationHeader</li>
<li>MessageInformationHeaderRequired</li>
<li>UnsupportedExpirationType</li>
<li>InvalidMessage</li>
<li>FilteringNotSupported</li>
</ul>




