---
UID: NC:wincrypt.PFN_CERT_ENUM_SYSTEM_STORE
title: PFN_CERT_ENUM_SYSTEM_STORE (wincrypt.h)
author: windows-sdk-content
description: The CertEnumSystemStoreCallback callback function formats and presents information on each system store found by a call to CertEnumSystemStore.
old-location: security\certenumsystemstorecallback.htm
tech.root: SecCrypto
ms.assetid: f070a9bd-be0b-49d0-9cab-a5d6f05d4e22
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CERT_SYSTEM_STORE_LOCATION_MASK, CERT_SYSTEM_STORE_RELOCATE_FLAG, CertEnumSystemStoreCallback, PFN_CERT_ENUM_SYSTEM_STORE, PFN_CERT_ENUM_SYSTEM_STORE callback, PFN_CERT_ENUM_SYSTEM_STORE callback function [Security], security.certenumsystemstorecallback, wincrypt/PFN_CERT_ENUM_SYSTEM_STORE
ms.topic: callback
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CERT_ENUM_SYSTEM_STORE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



