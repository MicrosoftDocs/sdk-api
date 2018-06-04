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

# ICertAdmin2::ImportKey


## -description


The <b>ImportKey</b> method adds an encrypted key set to an item in the Certificate Services database. The  key set is encrypted to one or several key recovery agent (KRA) certificates.


## -parameters




### -param strConfig [in]

String value that represents a valid configuration string for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA)  in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>ImportKey</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param RequestId [in]

<b>LONG</b> value that represents the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a> ID in the Certificates Services database. If the serial number (passed in as <i>strCertHash</i>) is to be used instead of the request ID, use zero for this value.


### -param strCertHash [in]

String value that represents the certificate hash. For <i>strCertHash</i> to be used, you must specify a value of zero for <i>RequestId</i>.


### -param Flags [in]

Specifies the format of the key. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_IN_BASE64HEADER"></a><a id="cr_in_base64header"></a><dl>
<dt><b>CR_IN_BASE64HEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 format with begin or end.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_BASE64"></a><a id="cr_in_base64"></a><dl>
<dt><b>CR_IN_BASE64</b></dt>
</dl>
</td>
<td width="60%">
BASE64 format without begin or end.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_BINARY"></a><a id="cr_in_binary"></a><dl>
<dt><b>CR_IN_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary format.

</td>
</tr>
</table>
 

Additionally, the following value can be combined with the format value by using a bitwise-<b>OR</b> operation.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IKF_OVERWRITE"></a><a id="ikf_overwrite"></a><dl>
<dt><b>IKF_OVERWRITE</b></dt>
</dl>
</td>
<td width="60%">
Any existing KRA encoded information is overwritten.

</td>
</tr>
</table>
 


### -param strKey [in]

String value that represents the KRA key information.


## -see-also




<a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin2</a>
 

 

