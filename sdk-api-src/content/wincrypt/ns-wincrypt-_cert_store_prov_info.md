---
UID: NS:wincrypt._CERT_STORE_PROV_INFO
title: "_CERT_STORE_PROV_INFO"
author: windows-sdk-content
description: Contains information returned by the installed CertDllOpenStoreProv function when a store is opened by using the CertOpenStore function.
old-location: security\cert_store_prov_info.htm
old-project: SecCrypto
ms.assetid: dc6789a7-09a5-467a-b2e4-16acfa25b5f6
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PCERT_STORE_PROV_INFO, CERT_STORE_PROV_CLOSE_FUNC, CERT_STORE_PROV_CONTROL_FUNC, CERT_STORE_PROV_DELETED_FLAG, CERT_STORE_PROV_DELETE_CERT_FUNC, CERT_STORE_PROV_DELETE_CRL_FUNC, CERT_STORE_PROV_DELETE_CTL_FUNC, CERT_STORE_PROV_EXTERNAL_FLAG, CERT_STORE_PROV_FIND_CERT_FUNC, CERT_STORE_PROV_FIND_CRL_FUNC, CERT_STORE_PROV_FIND_CTL_FUNC, CERT_STORE_PROV_FREE_FIND_CERT_FUNC, CERT_STORE_PROV_FREE_FIND_CRL_FUNC, CERT_STORE_PROV_FREE_FIND_CTL_FUNC, CERT_STORE_PROV_GET_CERT_PROPERTY_FUNC, CERT_STORE_PROV_GET_CRL_PROPERTY_FUNC, CERT_STORE_PROV_GET_CTL_PROPERTY_FUNC, CERT_STORE_PROV_INFO, CERT_STORE_PROV_INFO structure [Security], CERT_STORE_PROV_LM_SYSTEM_STORE_FLAG, CERT_STORE_PROV_NO_PERSIST_FLAG, CERT_STORE_PROV_READ_CERT_FUNC, CERT_STORE_PROV_READ_CRL_FUNC, CERT_STORE_PROV_READ_CTL_FUNC, CERT_STORE_PROV_SET_CERT_PROPERTY_FUNC, CERT_STORE_PROV_SET_CRL_PROPERTY_FUNC, CERT_STORE_PROV_SET_CTL_PROPERTY_FUNC, CERT_STORE_PROV_SYSTEM_STORE_FLAG, CERT_STORE_PROV_WRITE_CERT_FUNC, CERT_STORE_PROV_WRITE_CRL_FUNC, CERT_STORE_PROV_WRITE_CTL_FUNC, PCERT_STORE_PROV_INFO, PCERT_STORE_PROV_INFO structure pointer [Security], _CERT_STORE_PROV_INFO, _crypto2_cert_store_prov_info, security.cert_store_prov_info, wincrypt/CERT_STORE_PROV_INFO, wincrypt/PCERT_STORE_PROV_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: CERT_STORE_PROV_INFO, *PCERT_STORE_PROV_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_STORE_PROV_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_STORE_PROV_INFO structure


## -description


The <b>CERT_STORE_PROV_INFO</b> structure contains information returned by the installed 
<a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a>  function when a store is opened by using the  
<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> function.

When opening a store, the  <a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>  function sets all fields in the <b>CERT_STORE_PROV_INFO</b> structure to zero except <b>cbSize</b>, which is set to the size of <b>CERT_STORE_PROV_INFO</b>. The structure is updated by the <a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a> installable function. If there are no additional callback functions to be called, then <b>cStoreProvFunc</b> remains zero upon return.


## -struct-fields




### -field cbSize

Contains the size, in bytes, of this structure.


### -field cStoreProvFunc

Contains the number of elements in the <b>rgpvStoreProvFunc</b> array. This count must include any <b>NULL</b> values that are used in indexes prior to the last callback function implemented. For example, if only one callback function is implemented, but it is at index 2 (<b>CERT_STORE_PROV_WRITE_CERT_FUNC</b>), with <b>NULL</b> for indexes 0 and 1, then the number 3 should be passed for this parameter.


### -field rgpvStoreProvFunc

An array of pointers to the callback functions that are implemented by the provider. This array is indexed by the values given in the following table, and they must be in the order shown. The associated callback function is shown as well. All callback functions that are not implemented must be set to <b>NULL</b>. The array does not have to contain all callback function indexes, it only needs to contain the highest callback function index implemented. For example, if only the <b>CERT_STORE_PROV_WRITE_CERT_FUNC</b> (2) callback function is implemented, the array only needs to contain three elements.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_CLOSE_FUNC"></a><a id="cert_store_prov_close_func"></a><dl>
<dt><b>CERT_STORE_PROV_CLOSE_FUNC</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/2d0aa2c2-e79f-485c-ad47-6d9672c778da">CertStoreProvCloseCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_READ_CERT_FUNC"></a><a id="cert_store_prov_read_cert_func"></a><dl>
<dt><b>CERT_STORE_PROV_READ_CERT_FUNC</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/9073f41e-19cd-46af-9e05-3f55607802c3">CertStoreProvReadCertCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_WRITE_CERT_FUNC"></a><a id="cert_store_prov_write_cert_func"></a><dl>
<dt><b>CERT_STORE_PROV_WRITE_CERT_FUNC</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/97cc488a-7993-4b48-a4b4-cb13c6168226">CertStoreProvWriteCertCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_DELETE_CERT_FUNC"></a><a id="cert_store_prov_delete_cert_func"></a><dl>
<dt><b>CERT_STORE_PROV_DELETE_CERT_FUNC</b></dt>
<dt>3 (0x3)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/0ae64bbc-05f6-4fc2-a05d-895654b4b97d">CertStoreProvDeleteCertCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_SET_CERT_PROPERTY_FUNC"></a><a id="cert_store_prov_set_cert_property_func"></a><dl>
<dt><b>CERT_STORE_PROV_SET_CERT_PROPERTY_FUNC</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/03d7e1f6-030f-4eae-b76d-5465748d9583">CertStoreProvSetCertPropertyCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_READ_CRL_FUNC"></a><a id="cert_store_prov_read_crl_func"></a><dl>
<dt><b>CERT_STORE_PROV_READ_CRL_FUNC</b></dt>
<dt>5 (0x5)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/9644c200-1b55-4287-8d98-27b5a8d38c90">CertStoreProvReadCRLCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_WRITE_CRL_FUNC"></a><a id="cert_store_prov_write_crl_func"></a><dl>
<dt><b>CERT_STORE_PROV_WRITE_CRL_FUNC</b></dt>
<dt>6 (0x6)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/ba259770-4462-4d1e-bd60-8572612fe032">CertStoreProvWriteCRLCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_DELETE_CRL_FUNC"></a><a id="cert_store_prov_delete_crl_func"></a><dl>
<dt><b>CERT_STORE_PROV_DELETE_CRL_FUNC</b></dt>
<dt>7 (0x7)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/aa93cfaf-238f-4d77-a1cd-433a856ed133">CertStoreProvDeleteCRLCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_SET_CRL_PROPERTY_FUNC"></a><a id="cert_store_prov_set_crl_property_func"></a><dl>
<dt><b>CERT_STORE_PROV_SET_CRL_PROPERTY_FUNC</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/98ad9b24-8d7d-4fbe-8fd8-089f1ddfbff0">CertStoreProvSetCRLPropertyCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_READ_CTL_FUNC"></a><a id="cert_store_prov_read_ctl_func"></a><dl>
<dt><b>CERT_STORE_PROV_READ_CTL_FUNC</b></dt>
<dt>9 (0x9)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/09fbf42d-ed7a-4b1d-bad6-3bf8f216603c">CertStoreProvReadCTL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_WRITE_CTL_FUNC"></a><a id="cert_store_prov_write_ctl_func"></a><dl>
<dt><b>CERT_STORE_PROV_WRITE_CTL_FUNC</b></dt>
<dt>10 (0xA)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/91344133-0785-4c4f-8df3-83301cf85e70">CertStoreProvWriteCTL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_DELETE_CTL_FUNC"></a><a id="cert_store_prov_delete_ctl_func"></a><dl>
<dt><b>CERT_STORE_PROV_DELETE_CTL_FUNC</b></dt>
<dt>11 (0xB)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/6cda772f-7e94-414d-99fc-a90451ac0ccf">CertStoreProvDeleteCTL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_SET_CTL_PROPERTY_FUNC"></a><a id="cert_store_prov_set_ctl_property_func"></a><dl>
<dt><b>CERT_STORE_PROV_SET_CTL_PROPERTY_FUNC</b></dt>
<dt>12 (0xC)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/d062c875-b8c1-454f-8a0d-2ada74e5028d">CertStoreProvSetCTLProperty</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_CONTROL_FUNC"></a><a id="cert_store_prov_control_func"></a><dl>
<dt><b>CERT_STORE_PROV_CONTROL_FUNC</b></dt>
<dt>13 (0xD)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/0725d562-d04c-4fde-97f4-a294290266ee">CertStoreProvControl</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FIND_CERT_FUNC"></a><a id="cert_store_prov_find_cert_func"></a><dl>
<dt><b>CERT_STORE_PROV_FIND_CERT_FUNC</b></dt>
<dt>14 (0xE)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/1129a372-4d7c-454e-969b-26a1d6037bc0">CertStoreProvFindCert</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FREE_FIND_CERT_FUNC"></a><a id="cert_store_prov_free_find_cert_func"></a><dl>
<dt><b>CERT_STORE_PROV_FREE_FIND_CERT_FUNC</b></dt>
<dt>15 (0xF)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/be882b56-027c-4540-9426-27d3c2b262e9">CertStoreProvFreeFindCert</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_GET_CERT_PROPERTY_FUNC"></a><a id="cert_store_prov_get_cert_property_func"></a><dl>
<dt><b>CERT_STORE_PROV_GET_CERT_PROPERTY_FUNC</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/827e0331-1f87-4891-8cc1-de1bcbad2963">CertStoreProvGetCertProperty</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FIND_CRL_FUNC"></a><a id="cert_store_prov_find_crl_func"></a><dl>
<dt><b>CERT_STORE_PROV_FIND_CRL_FUNC</b></dt>
<dt>17 (0x11)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/caf218f5-f379-4cb6-bb4b-4767b846d45c">CertStoreProvFindCRL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FREE_FIND_CRL_FUNC"></a><a id="cert_store_prov_free_find_crl_func"></a><dl>
<dt><b>CERT_STORE_PROV_FREE_FIND_CRL_FUNC</b></dt>
<dt>18 (0x12)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/e90609f6-63cd-40eb-bd5a-289473daa5bb">CertStoreProvFreeFindCRL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_GET_CRL_PROPERTY_FUNC"></a><a id="cert_store_prov_get_crl_property_func"></a><dl>
<dt><b>CERT_STORE_PROV_GET_CRL_PROPERTY_FUNC</b></dt>
<dt>19 (0x13)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/b02f4f92-952a-4625-a7d4-6e78e542774e">CertStoreProvGetCRLProperty</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FIND_CTL_FUNC"></a><a id="cert_store_prov_find_ctl_func"></a><dl>
<dt><b>CERT_STORE_PROV_FIND_CTL_FUNC</b></dt>
<dt>20 (0x14)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/0b465e6e-fb5c-4621-a968-c2cdcab0ea15">CertStoreProvFindCTL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FREE_FIND_CTL_FUNC"></a><a id="cert_store_prov_free_find_ctl_func"></a><dl>
<dt><b>CERT_STORE_PROV_FREE_FIND_CTL_FUNC</b></dt>
<dt>21 (0x15)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/04e62a4e-4542-4225-8750-fabbda5adf0d">CertStoreProvFreeFindCTL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_GET_CTL_PROPERTY_FUNC"></a><a id="cert_store_prov_get_ctl_property_func"></a><dl>
<dt><b>CERT_STORE_PROV_GET_CTL_PROPERTY_FUNC</b></dt>
<dt>22 (0x16)</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/65309715-65b4-4608-960d-3404e68800a2">CertStoreProvGetCTLProperty</a>


</td>
</tr>
</table>
 


### -field hStoreProv

A 32-bit, application-defined value that is the first parameter passed to all callbacks. An application can specify the contents of this member as desired. Typically, this is a pointer to data that is specific to the application, such as provider state information for each store opened.


### -field dwStoreProvFlags

Contains a set of flags that specify how the provider works. Contains zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_EXTERNAL_FLAG"></a><a id="cert_store_prov_external_flag"></a><dl>
<dt><b>CERT_STORE_PROV_EXTERNAL_FLAG</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
The provider stores <a href="https://msdn.microsoft.com/library/windows/hardware/mt484158">certificates</a>, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation lists</a>, and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust lists</a> that are external to the store's cache.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_DELETED_FLAG"></a><a id="cert_store_prov_deleted_flag"></a><dl>
<dt><b>CERT_STORE_PROV_DELETED_FLAG</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
The store was successfully deleted. The <a href="https://msdn.microsoft.com/2d0aa2c2-e79f-485c-ad47-6d9672c778da">CertStoreProvCloseCallback</a> callback is not called.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_NO_PERSIST_FLAG"></a><a id="cert_store_prov_no_persist_flag"></a><dl>
<dt><b>CERT_STORE_PROV_NO_PERSIST_FLAG</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
By default, the provider will persist changes that are made to the store. If this flag is set, the provider does not persist the changes made to the store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_SYSTEM_STORE_FLAG"></a><a id="cert_store_prov_system_store_flag"></a><dl>
<dt><b>CERT_STORE_PROV_SYSTEM_STORE_FLAG</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">
The provider persists contexts to a system store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_LM_SYSTEM_STORE_FLAG"></a><a id="cert_store_prov_lm_system_store_flag"></a><dl>
<dt><b>CERT_STORE_PROV_LM_SYSTEM_STORE_FLAG</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
The provider persists contexts to a LocalMachine system store.

</td>
</tr>
</table>
 


### -field hStoreProvFuncAddr2

Contains the handle returned by 
<a href="https://msdn.microsoft.com/2eef6109-a840-48c6-936c-ec0875039c39">CryptGetOIDFunctionAddress</a>. 
<a href="https://msdn.microsoft.com/a93fdd65-359e-4046-910d-347c3af01280">CertCloseStore</a> calls 
<a href="https://msdn.microsoft.com/cacacff3-25b7-4ed4-885b-b4b0b326628f">CryptFreeOIDFunctionAddress</a> to free a non-null <b>hStoreProvFuncAddr2</b>. This allows the callback to call one other installable function that will be freed when the store is closed.

