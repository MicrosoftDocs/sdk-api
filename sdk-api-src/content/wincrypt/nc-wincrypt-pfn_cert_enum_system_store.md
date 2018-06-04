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

# PFN_CERT_ENUM_SYSTEM_STORE callback function


## -description


The <b>CertEnumSystemStoreCallback</b> 
	callback function formats and presents information on each system store found by a call to 
	<a href="https://msdn.microsoft.com/fd9cb23b-e4a3-41cb-8f0a-30f4e813c6ac">CertEnumSystemStore</a>.


## -parameters




### -param *pvSystemStore [in]

A pointer to information on the system store found by a call to 
	<a href="https://msdn.microsoft.com/fd9cb23b-e4a3-41cb-8f0a-30f4e813c6ac">CertEnumSystemStore</a>. Where appropriate, this argument will contain a leading computer name or service name prefix.


### -param dwFlags [in]

Flag used to call for an alteration of the presentation. This can be a bitwise <b>OR</b> of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_SYSTEM_STORE_LOCATION_MASK"></a><a id="cert_system_store_location_mask"></a><dl>
<dt><b>CERT_SYSTEM_STORE_LOCATION_MASK</b></dt>
</dl>
</td>
<td width="60%">
Specifies the location of the system store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SYSTEM_STORE_RELOCATE_FLAG"></a><a id="cert_system_store_relocate_flag"></a><dl>
<dt><b>CERT_SYSTEM_STORE_RELOCATE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
If set, the <i>pvSystemStore</i> parameter points to a CERT_SYSTEM_STORE_RELOCATE_PARA structure. If not set, <i>pvSystemStore</i> points to a <b>NULL</b>-terminated Unicode string.

</td>
</tr>
</table>
 


### -param pStoreInfo [in]

A pointer to a 
	    <a href="https://msdn.microsoft.com/9c17ebd9-423b-4063-bdc3-6be70ceb8623">CERT_SYSTEM_STORE_INFO</a> structure that contains information about the store.


### -param *pvReserved [in]

Reserved for future use.


### -param *pvArg [in]

A pointer to information passed to the callback function in the <i>pvArg</i> 
	 passed to <a href="https://msdn.microsoft.com/fd9cb23b-e4a3-41cb-8f0a-30f4e813c6ac">CertEnumSystemStore</a>.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.
						

To stop the enumeration, the function must return <b>FALSE</b>.



