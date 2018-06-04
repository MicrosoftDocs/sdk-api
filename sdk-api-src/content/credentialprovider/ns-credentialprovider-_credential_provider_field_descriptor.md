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

# _CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR structure


## -description


Describes a single field in a credential. For example, a string or a user image.


## -struct-fields




### -field dwFieldID

Type: <b>DWORD</b>

The unique ID of the field. Fields should have a unique identifier compared to all other fields on a given credential provider. This is true regardless of whether the fields are displayed or hidden.


### -field cpft

Type: <b><a href="https://msdn.microsoft.com/5af9f007-9588-4574-a5ce-3f01ec0b45e8">CREDENTIAL_PROVIDER_FIELD_TYPE</a></b>

The field type.


### -field pszLabel

Type: <b>LPWSTR</b>

A pointer to a buffer containing the friendly name of the field as a null-terminated Unicode string. This is used for accessibility and queuing purposes. For example, some standard fields would have friend names of "Username", "Password", and "Log On To".


### -field guidFieldType

Type: <b>GUID</b>

A GUID that uniquely identifies a type of field. This member enables you to wrap functionality provided by existing credential providers in their own providers. Wrapping credential providers is not recommended as it can lead to unexpected behavior that disables in-box credential providers.

The following table lists the <i>guidFieldType</i> values supported by Windows. These are defined in Shlguid.h. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CPFG_LOGON_USERNAME"></a><a id="cpfg_logon_username"></a><dl>
<dt><b>CPFG_LOGON_USERNAME</b></dt>
<dt>da15bbe8-954sd-4fd3-b0f4-1fb5b90b174b</dt>
</dl>
</td>
<td width="60%">
The user name entered into a text box.

</td>
</tr>
<tr>
<td width="40%"><a id="CPFG_LOGON_PASSWORD"></a><a id="cpfg_logon_password"></a><dl>
<dt><b>CPFG_LOGON_PASSWORD</b></dt>
<dt>60624cfa-a477-47b1-8a8e-3a4a19981827</dt>
</dl>
</td>
<td width="60%">
The password entered into a text box.

</td>
</tr>
<tr>
<td width="40%"><a id="CPFG_SMARTCARD_USERNAME"></a><a id="cpfg_smartcard_username"></a><dl>
<dt><b>CPFG_SMARTCARD_USERNAME</b></dt>
<dt>3e1ecf69-568c-4d96-9d59-46444174e2d6</dt>
</dl>
</td>
<td width="60%">
The user name obtained from an inserted smart card.

</td>
</tr>
<tr>
<td width="40%"><a id="CPFG_SMARTCARD_PIN"></a><a id="cpfg_smartcard_pin"></a><dl>
<dt><b>CPFG_SMARTCARD_PIN</b></dt>
<dt>4fe5263b-9181-46c1-b0a4-9dedd4db7dea</dt>
</dl>
</td>
<td width="60%">
The PIN obtained from an inserted smart card.

</td>
</tr>
<tr>
<td width="40%"><a id="CPFG_CREDENTIAL_PROVIDER_LOGO"></a><a id="cpfg_credential_provider_logo"></a><dl>
<dt><b>CPFG_CREDENTIAL_PROVIDER_LOGO</b></dt>
<dt>2d837775-f6cd-464e-a745-482fd0b47493</dt>
</dl>
</td>
<td width="60%">
<b>Introduced in Windows 8</b>: The image used to represent a credential provider on the logon page.

</td>
</tr>
<tr>
<td width="40%"><a id="CPFG_CREDENTIAL_PROVIDER_LABEL"></a><a id="cpfg_credential_provider_label"></a><dl>
<dt><b>CPFG_CREDENTIAL_PROVIDER_LABEL</b></dt>
<dt>286BBFF3-BAD4-438F-B007-79B7267C3D48</dt>
</dl>
</td>
<td width="60%">
<b>Introduced in Windows 8</b>: The label associated with a credential provider on the logon page.

</td>
</tr>
</table>
 


## -remarks



Each UI element presented to the user on a tile is defined by the credential provider as a field. The <b>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</b> is how the credential provider identifies the fields. Once a field has been defined for a particular usage scenario, it can not be added to or subtracted from. Credential providers need to fully define all of their fields before enumerating tiles. If fields are going to appear or disappear as part of the credential acquisition process, those fields still not to be defined ahead of time. Use <a href="https://msdn.microsoft.com/4cc7858c-483b-4fac-96ba-8962bc362422">CREDENTIAL_PROVIDER_FIELD_STATE</a> to hide or display the fields as necessary.



