---
UID: NF:wincrypt.CertUnregisterSystemStore
title: CertUnregisterSystemStore function
author: windows-sdk-content
description: The CertUnregisterSystemStore function unregisters a specified system store.
old-location: security\certunregistersystemstore.htm
old-project: seccrypto
ms.assetid: 958e4185-4c37-450c-abfc-91b95593227e
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CERT_STORE_DELETE_FLAG, CERT_SYSTEM_STORE_RELOCATE_FLAG, CertUnregisterSystemStore, CertUnregisterSystemStore function [Security], _crypto2_certunregistersystemstore, security.certunregistersystemstore, wincrypt/CertUnregisterSystemStore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertUnregisterSystemStore
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertUnregisterSystemStore function


## -description


The <b>CertUnregisterSystemStore</b> function unregisters a specified system store.


## -parameters




### -param pvSystemStore [in]

Identifies the system store to be unregistered. It points either to a null-terminated Unicode string or to a 
<a href="https://msdn.microsoft.com/3bcb9b64-b9cf-48b2-bfd1-0836b3d221af">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure. For information about using the structure and on appending a ServiceName or ComputerName to the end of the system store name string, see 
<a href="https://msdn.microsoft.com/b6f72826-92ab-4e21-8db9-eb053663148b">CertRegisterSystemStore</a>.


### -param dwFlags [in]

The high word of the <i>dwFlags</i> parameter specifies the location of the system store. For information about defined high-word flags and on appending ServiceName, UserNames, and ComputerNames to the end of the system store name, see 
<a href="https://msdn.microsoft.com/b6f72826-92ab-4e21-8db9-eb053663148b">CertRegisterSystemStore</a>. 




The following low-word values are also defined and can be combined with high-word values using a bitwise-<b>OR</b> operation.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_SYSTEM_STORE_RELOCATE_FLAG"></a><a id="cert_system_store_relocate_flag"></a><dl>
<dt><b>CERT_SYSTEM_STORE_RELOCATE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The system store is not in its default registry location and <i>pvSystemStore</i> must be a pointer to a 
<a href="https://msdn.microsoft.com/3bcb9b64-b9cf-48b2-bfd1-0836b3d221af">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_DELETE_FLAG"></a><a id="cert_store_delete_flag"></a><dl>
<dt><b>CERT_STORE_DELETE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The system store is deleted after it has been unregistered.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/3bcb9b64-b9cf-48b2-bfd1-0836b3d221af">CERT_SYSTEM_STORE_RELOCATE_PARA</a>



<a href="https://msdn.microsoft.com/5804d565-5129-4e6d-8b3d-9bd938807740">CertEnumPhysicalStore</a>



<a href="https://msdn.microsoft.com/fd9cb23b-e4a3-41cb-8f0a-30f4e813c6ac">CertEnumSystemStore</a>



<a href="https://msdn.microsoft.com/86408e6f-0732-4cb4-85cd-840b9d98b973">CertEnumSystemStoreLocation</a>



<a href="https://msdn.microsoft.com/e301c76d-cacd-441a-b925-754b07e4bfa9">CertRegisterPhysicalStore</a>



<a href="https://msdn.microsoft.com/b6f72826-92ab-4e21-8db9-eb053663148b">CertRegisterSystemStore</a>



<a href="https://msdn.microsoft.com/06480a2f-5a94-4cf5-9774-ceb9499e1d44">CertUnregisterPhysicalStore</a>



<a href="cryptography_functions.htm">Certificate Store Functions</a>
 

 

