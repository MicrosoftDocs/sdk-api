---
UID: NF:certadm.ICertAdmin2.SetCAProperty
title: ICertAdmin2::SetCAProperty
author: windows-sdk-content
description: Sets a property value for the certification authority (CA).
old-location: security\icertadmin2_setcaproperty.htm
tech.root: seccrypto
ms.assetid: 29570a8f-41d4-4c6a-88d0-97d6aa9d0784
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CR_PROP_KRACERT, CR_PROP_KRACERTCOUNT, CR_PROP_KRACERTUSEDCOUNT, CR_PROP_ROLESEPARATIONENABLED, CR_PROP_TEMPLATES, ICertAdmin2 interface [Security],SetCAProperty method, ICertAdmin2.SetCAProperty, ICertAdmin2::SetCAProperty, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, SetCAProperty, SetCAProperty method [Security], SetCAProperty method [Security],ICertAdmin2 interface, certadm/ICertAdmin2::SetCAProperty, security.icertadmin2_setcaproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2.SetCAProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertAdmin2::SetCAProperty


## -description


The <b>SetCAProperty</b> method sets a property value for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA).


## -parameters




### -param strConfig [in]

String value that represents a valid configuration string for the CA in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>.<div class="alert"><b>Important</b>  <b>SetCAProperty</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>



### -param PropId [in]

Specifies one of the following property identifiers.

For information about all CA properties, including those that are read-only, see <a href="https://msdn.microsoft.com/8eaa2e36-4358-4abd-a7c2-2c9768766597">ICertAdmin2::GetCAProperty</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_KRACERT"></a><a id="cr_prop_kracert"></a><dl>
<dt><b>CR_PROP_KRACERT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The CA's key recovery agent (KRA) certificate.

Data format: binary, indexed.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_KRACERTCOUNT"></a><a id="cr_prop_kracertcount"></a><dl>
<dt><b>CR_PROP_KRACERTCOUNT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Number of KRA certificates for the CA.

Data format: <b>Long</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_KRACERTUSEDCOUNT"></a><a id="cr_prop_kracertusedcount"></a><dl>
<dt><b>CR_PROP_KRACERTUSEDCOUNT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Number of KRA certificates used by the CA.

Data format: <b>Long</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_ROLESEPARATIONENABLED"></a><a id="cr_prop_roleseparationenabled"></a><dl>
<dt><b>CR_PROP_ROLESEPARATIONENABLED</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Value that specifies whether role separation is enabled.

Data format: <b>Long</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_TEMPLATES"></a><a id="cr_prop_templates"></a><dl>
<dt><b>CR_PROP_TEMPLATES</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
List of templates supported by the CA.

Data format: <b>String</b>.

</td>
</tr>
</table>
 


### -param PropIndex [in]

If the <i>PropId</i> parameter is indexed, the zero-based index to use when retrieving the property value. If <i>PropId</i> is not indexed, this value is ignored.


### -param PropType [in]

Specifies the type of the property. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_LONG"></a><a id="proptype_long"></a><dl>
<dt><b>PROPTYPE_LONG</b></dt>
</dl>
</td>
<td width="60%">
Signed <b>Long</b> data.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_DATE"></a><a id="proptype_date"></a><dl>
<dt><b>PROPTYPE_DATE</b></dt>
</dl>
</td>
<td width="60%">
Date/Time (reserved for future use).

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_BINARY"></a><a id="proptype_binary"></a><dl>
<dt><b>PROPTYPE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary data.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_STRING"></a><a id="proptype_string"></a><dl>
<dt><b>PROPTYPE_STRING</b></dt>
</dl>
</td>
<td width="60%">
<a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> <b>String</b> data.

</td>
</tr>
</table>
 


### -param pvarPropertyValue [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td>
A pointer to a <b>VARIANT</b> that specifies the property value.

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>
A <b>Variant</b> that specifies the property value.

</td>
</tr>
</table>

## -returns



<h3>VB</h3>
If the function is successful, the return value is S_OK.

 
If the function fails, the return value is an <b>HRESULT</b> that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin2</a>



<a href="https://msdn.microsoft.com/8eaa2e36-4358-4abd-a7c2-2c9768766597">ICertAdmin2::GetCAProperty</a>
 

 

