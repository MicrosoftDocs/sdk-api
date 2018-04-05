---
UID: NF:azroles.IAzApplication.SetProperty
title: IAzApplication::SetProperty method
author: windows-driver-content
description: Sets the specified value to the IAzApplication object property with the specified property ID.
old-location: security\iazapplication_setproperty.htm
old-project: SecAuthZ
ms.assetid: 077ed5a9-7a38-4477-9fac-1f0b88ab0d33
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: AZ_PROP_APPLICATION_AUTHZ_INTERFACE_CLSID, AZ_PROP_APPLICATION_DATA, AZ_PROP_APPLICATION_INTERFACE_CLSID, AZ_PROP_APPLICATION_VERSION, AZ_PROP_APPLY_STORE_SACL, AZ_PROP_DESCRIPTION, AZ_PROP_GENERATE_AUDITS, AZ_PROP_NAME, AzApplication object [Security], SetProperty method, IAzApplication, IAzApplication interface [Security], SetProperty method, IAzApplication::SetProperty, SetProperty method [Security], SetProperty method [Security], AzApplication object, SetProperty method [Security], IAzApplication interface, SetProperty,IAzApplication.SetProperty, azroles/IAzApplication::SetProperty, security.iazapplication_setproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzApplication.SetProperty
-	AzApplication.SetProperty
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::SetProperty method


## -description


The <b>SetProperty</b> method sets the specified value to the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object property  with the specified property ID.


## -parameters




### -param lPropId [in]

Property ID of the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object property  to set. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_DATA"></a><a id="az_prop_application_data"></a><dl>
<dt><b>AZ_PROP_APPLICATION_DATA</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/7d7ec5c8-8032-437a-92b5-5c578deda6f9">ApplicationData</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_AUTHZ_INTERFACE_CLSID"></a><a id="az_prop_application_authz_interface_clsid"></a><dl>
<dt><b>AZ_PROP_APPLICATION_AUTHZ_INTERFACE_CLSID</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/d3dddd9c-a715-4697-bcca-ba12cead3b61">AuthzInterfaceClsid</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_VERSION"></a><a id="az_prop_application_version"></a><dl>
<dt><b>AZ_PROP_APPLICATION_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/dn973197">Version</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLY_STORE_SACL"></a><a id="az_prop_apply_store_sacl"></a><dl>
<dt><b>AZ_PROP_APPLY_STORE_SACL</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/722b0693-a11f-434a-a278-780619b0077a">ApplyStoreSacl</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GENERATE_AUDITS"></a><a id="az_prop_generate_audits"></a><dl>
<dt><b>AZ_PROP_GENERATE_AUDITS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/c35f612e-4a2c-46b6-913a-26b0819394f4">GenerateAudits</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> property

</td>
</tr>
</table>
 


### -param varProp [in]

Value to set to the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object property  specified by the <i>lPropId</i> parameter. The type of data that must be used depends on the value of the <i>lPropId</i> parameter.

<table>
<tr>
<th><i>lPropId</i> value</th>
<th>Data type (C++/Visual Basic)</th>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_DATA"></a><a id="az_prop_application_data"></a><dl>
<dt><b>AZ_PROP_APPLICATION_DATA</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_INTERFACE_CLSID"></a><a id="az_prop_application_interface_clsid"></a><dl>
<dt><b>AZ_PROP_APPLICATION_INTERFACE_CLSID</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_VERSION"></a><a id="az_prop_application_version"></a><dl>
<dt><b>AZ_PROP_APPLICATION_VERSION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLY_STORE_SACL"></a><a id="az_prop_apply_store_sacl"></a><dl>
<dt><b>AZ_PROP_APPLY_STORE_SACL</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GENERATE_AUDITS"></a><a id="az_prop_generate_audits"></a><dl>
<dt><b>AZ_PROP_GENERATE_AUDITS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>BSTR</b>/<b>String</b>

</td>
</tr>
</table>
 


### -param varReserved [in, optional]

Reserved for future use.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/d00d55a1-884f-46c2-b80b-f90ce8f5c648">Submit</a> method to persist any changes made by this method.



