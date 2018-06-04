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

# _SECURITY_PACKAGE_OPTIONS structure


## -description


Specifies information about a security package. This structure is used by the <a href="https://msdn.microsoft.com/35b993d2-87a0-46d0-991f-88358b0cc5e6">AddSecurityPackage</a> function.


## -struct-fields




### -field Size

The size, in bytes, of this structure.


### -field Type

The type of security package. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_OPTIONS_TYPE_UNKNOWN"></a><a id="secpkg_options_type_unknown"></a><dl>
<dt><b>SECPKG_OPTIONS_TYPE_UNKNOWN</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The package type is not known.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_OPTIONS_TYPE_LSA"></a><a id="secpkg_options_type_lsa"></a><dl>
<dt><b>SECPKG_OPTIONS_TYPE_LSA</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The security package is an <a href="https://msdn.microsoft.com/a5bc4c5d-6e8e-4cdf-962e-4284997c75e7">LSA authentication</a> package.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_OPTIONS_TYPE_SSPI"></a><a id="secpkg_options_type_sspi"></a><dl>
<dt><b>SECPKG_OPTIONS_TYPE_SSPI</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The security package is a <a href="https://msdn.microsoft.com/79ed7c51-4191-40b2-8d5f-06157f5b99be">Security Support Provider Interface</a> (SSPI) package.

</td>
</tr>
</table>
 


### -field Flags

This member is reserved. Do not use it.


### -field SignatureSize

The size, in bytes, of a digital signature for this security package.


### -field Signature

A digital signature for this security package.

