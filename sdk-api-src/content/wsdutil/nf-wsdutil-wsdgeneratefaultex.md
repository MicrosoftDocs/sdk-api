---
UID: NF:wsdutil.WSDGenerateFaultEx
title: WSDGenerateFaultEx function (wsdutil.h)
description: Generates a SOAP fault. (WSDGenerateFaultEx)
helpviewer_keywords: ["DataEncodingUnknown","MustUnderstand","Receiver","Sender","VersionMismatch","WSDGenerateFaultEx","WSDGenerateFaultEx function","ncd.wsdgeneratefaultex","wsdutil/WSDGenerateFaultEx"]
old-location: ncd\wsdgeneratefaultex.htm
tech.root: ncd
ms.assetid: 11cdd975-cc06-4fdc-8d84-c419e2a2b5ff
ms.date: 12/05/2018
ms.keywords: DataEncodingUnknown, MustUnderstand, Receiver, Sender, VersionMismatch, WSDGenerateFaultEx, WSDGenerateFaultEx function, ncd.wsdgeneratefaultex, wsdutil/WSDGenerateFaultEx
req.header: wsdutil.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSDGenerateFaultEx
 - wsdutil/WSDGenerateFaultEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDGenerateFaultEx
---

# WSDGenerateFaultEx function


## -description

Generates a SOAP fault.

## -parameters

### -param pCode [in]

A SOAP fault code.


The list of possible fault codes follows. For a description of each fault code, see the 

<a href="https://www.w3.org/TR/2003/REC-soap12-part1-20030624/#faultcodes">SOAP Version 1.2 specification</a>.



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

### -param pSubCode [in]

A fault subcode.

### -param pReasons [in]

A <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_localized_string_list">WSD_LOCALIZED_STRING_LIST</a> structure that contains a list of localized reason codes.

### -param pszDetail [in]

Contains application-specific error information pertaining to the fault.

### -param ppFault [out]

A <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_fault">WSD_SOAP_FAULT</a> structure that contains the generated fault.  <i>ppFault</i> must be freed with a call to <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a>.

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
<i>pszCode</i> or <i>pReasons</i> is <b>NULL</b>.

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
