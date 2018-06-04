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

# _SECPKG_PARAMETERS structure


## -description


The <b>SECPKG_PARAMETERS</b> structure contains information about the computer system. This structure is used by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.


## -struct-fields




### -field Version

The version of the Security Support Provider Interface in use.


### -field MachineState

The state of the machine. The following table lists the valid values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_STATE_ENCRYPTION_PERMITTED"></a><a id="secpkg_state_encryption_permitted"></a><dl>
<dt><b>SECPKG_STATE_ENCRYPTION_PERMITTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> may use encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_STATE_STRONG_ENCRYPTION_PERMITTED"></a><a id="secpkg_state_strong_encryption_permitted"></a><dl>
<dt><b>SECPKG_STATE_STRONG_ENCRYPTION_PERMITTED</b></dt>
</dl>
</td>
<td width="60%">
The security package may use strong encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_STATE_DOMAIN_CONTROLLER"></a><a id="secpkg_state_domain_controller"></a><dl>
<dt><b>SECPKG_STATE_DOMAIN_CONTROLLER</b></dt>
</dl>
</td>
<td width="60%">
The machine is a domain controller.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_STATE_WORKSTATION"></a><a id="secpkg_state_workstation"></a><dl>
<dt><b>SECPKG_STATE_WORKSTATION</b></dt>
</dl>
</td>
<td width="60%">
The machine is a workstation with access to a network.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_STATE_STANDALONE"></a><a id="secpkg_state_standalone"></a><dl>
<dt><b>SECPKG_STATE_STANDALONE</b></dt>
</dl>
</td>
<td width="60%">
The machine is a stand-alone system.

</td>
</tr>
</table>
 


### -field SetupMode

Contains a nonzero value if setup is running.


### -field DomainSid

The security identifier of the primary domain.


### -field DomainName

The name of the primary domain.


### -field DnsDomainName

The Domain Name System (DNS) name of the primary domain.


### -field DomainGuid

The GUID of the primary domain.

