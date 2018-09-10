---
UID: NF:wincrypt.CertRegisterSystemStore
title: CertRegisterSystemStore function
author: windows-sdk-content
description: Registers a system store.
old-location: security\certregistersystemstore.htm
tech.root: seccrypto
ms.assetid: b6f72826-92ab-4e21-8db9-eb053663148b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CERT_STORE_CREATE_NEW_FLAG, CERT_SYSTEM_STORE_CURRENT_SERVICE, CERT_SYSTEM_STORE_CURRENT_USER, CERT_SYSTEM_STORE_LOCAL_MACHINE, CERT_SYSTEM_STORE_LOCAL_MACHINE_GROUP_POLICY, CERT_SYSTEM_STORE_RELOCATE_FLAG, CERT_SYSTEM_STORE_SERVICES, CERT_SYSTEM_STORE_USERS, CertRegisterSystemStore, CertRegisterSystemStore function [Security], _crypto2_certregistersystemstore, security.certregistersystemstore, wincrypt/CertRegisterSystemStore
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertRegisterSystemStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertRegisterSystemStore function


## -description


The <b>CertRegisterSystemStore</b> function registers a system store.


## -parameters




### -param pvSystemStore [in]

Identifies the system store to be registered. If CERT_SYSTEM_STORE_RELOCATE_FLAG is set in the <i>dwFlags</i> parameter, <i>pvSystemStore</i> points to a 
<a href="https://msdn.microsoft.com/3bcb9b64-b9cf-48b2-bfd1-0836b3d221af">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure. Otherwise, it points to a <b>null</b>-terminated Unicode string that names the system store. 




With appropriate settings in <i>dwFlags</i>, the identified store can be a system store on a remote local computer. Stores on remote computers can be registered with the computer name as a prefix to the name of the system store. For example, a remote local computer store can be registered with <i>pvSystemStore</i> pointing to the string "\\ComputerName\Trust" or "ComputerName\Trust".

Leading "\\" backslashes are optional before a ComputerName.


### -param dwFlags [in]

The high word of the <i>dwFlags</i> parameter is used to specify the location of the system store. 



						
						
						
						
					


The following high-word values are defined.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_SYSTEM_STORE_CURRENT_SERVICE"></a><a id="cert_system_store_current_service"></a><dl>
<dt><b>CERT_SYSTEM_STORE_CURRENT_SERVICE</b></dt>
</dl>
</td>
<td width="60%">
<i>pvSystemStore</i> can be a system store name that is prefixed with the ServiceName.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SYSTEM_STORE_CURRENT_USER"></a><a id="cert_system_store_current_user"></a><dl>
<dt><b>CERT_SYSTEM_STORE_CURRENT_USER</b></dt>
</dl>
</td>
<td width="60%">
<i>pvSystemStore</i> can be a system store name that is prefixed with the UserName.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SYSTEM_STORE_LOCAL_MACHINE"></a><a id="cert_system_store_local_machine"></a><dl>
<dt><b>CERT_SYSTEM_STORE_LOCAL_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
<i>pvSystemStore</i> can be a system store that is on a remote computer.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SYSTEM_STORE_LOCAL_MACHINE_GROUP_POLICY"></a><a id="cert_system_store_local_machine_group_policy"></a><dl>
<dt><b>CERT_SYSTEM_STORE_LOCAL_MACHINE_GROUP_POLICY</b></dt>
</dl>
</td>
<td width="60%">
<i>pvSystemStore</i> is a group policy store and can be on a remote computer.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SYSTEM_STORE_SERVICES"></a><a id="cert_system_store_services"></a><dl>
<dt><b>CERT_SYSTEM_STORE_SERVICES</b></dt>
</dl>
</td>
<td width="60%">
<i>pvSystemStore</i> must be a system store name prefixed with the ServiceName.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SYSTEM_STORE_USERS"></a><a id="cert_system_store_users"></a><dl>
<dt><b>CERT_SYSTEM_STORE_USERS</b></dt>
</dl>
</td>
<td width="60%">
<i>pvSystemStore</i> must be a system store name that is prefixed with the UserName.

</td>
</tr>
</table>
 

Stores on remote computers can be registered for CERT_SYSTEM_STORE_LOCAL_MACHINE, CERT_SYSTEM_STORE_SERVICES, CERT_SYSTEM_STORE_USERS, or CERT_SYSTEM_STORE_LOCAL_MACHINE_GROUP_POLICY.


The following low-word values are also defined and can be combined using a bitwise-<b>OR</b> operation with high-word values.



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
The system store is not in its default register location and <i>pvSystemStore</i> must be a pointer to a 
<a href="https://msdn.microsoft.com/3bcb9b64-b9cf-48b2-bfd1-0836b3d221af">CERT_SYSTEM_STORE_RELOCATE_PARA</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CREATE_NEW_FLAG"></a><a id="cert_store_create_new_flag"></a><dl>
<dt><b>CERT_STORE_CREATE_NEW_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The function fails if the system store already exists in the store location.

</td>
</tr>
</table>
 


### -param pStoreInfo [in]

Reserved for future use and must be set to <b>NULL</b>.


### -param pvReserved [in]

Reserved for future use and must be set to <b>NULL</b>.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero.




## -remarks



To unregister a system store that has been registered by this function, call <a href="https://msdn.microsoft.com/958e4185-4c37-450c-abfc-91b95593227e">CertUnregisterSystemStore</a>.


#### Examples

The following example shows adding a system store to a registry system store collection. For an example that includes the complete context for this example, see <a href="https://msdn.microsoft.com/bc4268ea-f657-4789-9d0a-6e5354508f86">Example C Program: Listing System and Physical Stores</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//--------------------------------------------------------------------
// Declare and initialize variables.

LPCWSTR pvSystemName= L"NEWSTORE";  // For this setting of 
                                    // dwFlags, the store name may 
                                    // be prefixed with a user name.
DWORD dwFlags= CERT_SYSTEM_STORE_CURRENT_USER;

if(CertRegisterSystemStore(
    pvSystemName,
    dwFlags,
    NULL,
    NULL))
{
  printf("System store %S is registered. \n",pvSystemName);
}
else
{
  printf("The system store did not register. \n");
  exit(1);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5804d565-5129-4e6d-8b3d-9bd938807740">CertEnumPhysicalStore</a>



<a href="https://msdn.microsoft.com/fd9cb23b-e4a3-41cb-8f0a-30f4e813c6ac">CertEnumSystemStore</a>



<a href="https://msdn.microsoft.com/86408e6f-0732-4cb4-85cd-840b9d98b973">CertEnumSystemStoreLocation</a>



<a href="https://msdn.microsoft.com/e301c76d-cacd-441a-b925-754b07e4bfa9">CertRegisterPhysicalStore</a>



<a href="https://msdn.microsoft.com/06480a2f-5a94-4cf5-9774-ceb9499e1d44">CertUnregisterPhysicalStore</a>



<a href="https://msdn.microsoft.com/958e4185-4c37-450c-abfc-91b95593227e">CertUnregisterSystemStore</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Certificate Store Functions</a>
 

 

