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
 

 

