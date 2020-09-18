---
UID: NS:wincrypt._CERT_STORE_PROV_INFO
title: CERT_STORE_PROV_INFO (wincrypt.h)
description: Contains information returned by the installed CertDllOpenStoreProv function when a store is opened by using the CertOpenStore function.
helpviewer_keywords: ["*PCERT_STORE_PROV_INFO","CERT_STORE_PROV_CLOSE_FUNC","CERT_STORE_PROV_CONTROL_FUNC","CERT_STORE_PROV_DELETED_FLAG","CERT_STORE_PROV_DELETE_CERT_FUNC","CERT_STORE_PROV_DELETE_CRL_FUNC","CERT_STORE_PROV_DELETE_CTL_FUNC","CERT_STORE_PROV_EXTERNAL_FLAG","CERT_STORE_PROV_FIND_CERT_FUNC","CERT_STORE_PROV_FIND_CRL_FUNC","CERT_STORE_PROV_FIND_CTL_FUNC","CERT_STORE_PROV_FREE_FIND_CERT_FUNC","CERT_STORE_PROV_FREE_FIND_CRL_FUNC","CERT_STORE_PROV_FREE_FIND_CTL_FUNC","CERT_STORE_PROV_GET_CERT_PROPERTY_FUNC","CERT_STORE_PROV_GET_CRL_PROPERTY_FUNC","CERT_STORE_PROV_GET_CTL_PROPERTY_FUNC","CERT_STORE_PROV_INFO","CERT_STORE_PROV_INFO structure [Security]","CERT_STORE_PROV_LM_SYSTEM_STORE_FLAG","CERT_STORE_PROV_NO_PERSIST_FLAG","CERT_STORE_PROV_READ_CERT_FUNC","CERT_STORE_PROV_READ_CRL_FUNC","CERT_STORE_PROV_READ_CTL_FUNC","CERT_STORE_PROV_SET_CERT_PROPERTY_FUNC","CERT_STORE_PROV_SET_CRL_PROPERTY_FUNC","CERT_STORE_PROV_SET_CTL_PROPERTY_FUNC","CERT_STORE_PROV_SYSTEM_STORE_FLAG","CERT_STORE_PROV_WRITE_CERT_FUNC","CERT_STORE_PROV_WRITE_CRL_FUNC","CERT_STORE_PROV_WRITE_CTL_FUNC","PCERT_STORE_PROV_INFO","PCERT_STORE_PROV_INFO structure pointer [Security]","_crypto2_cert_store_prov_info","security.cert_store_prov_info","wincrypt/CERT_STORE_PROV_INFO","wincrypt/PCERT_STORE_PROV_INFO"]
old-location: security\cert_store_prov_info.htm
tech.root: security
ms.assetid: dc6789a7-09a5-467a-b2e4-16acfa25b5f6
ms.date: 12/05/2018
ms.keywords: '*PCERT_STORE_PROV_INFO, CERT_STORE_PROV_CLOSE_FUNC, CERT_STORE_PROV_CONTROL_FUNC, CERT_STORE_PROV_DELETED_FLAG, CERT_STORE_PROV_DELETE_CERT_FUNC, CERT_STORE_PROV_DELETE_CRL_FUNC, CERT_STORE_PROV_DELETE_CTL_FUNC, CERT_STORE_PROV_EXTERNAL_FLAG, CERT_STORE_PROV_FIND_CERT_FUNC, CERT_STORE_PROV_FIND_CRL_FUNC, CERT_STORE_PROV_FIND_CTL_FUNC, CERT_STORE_PROV_FREE_FIND_CERT_FUNC, CERT_STORE_PROV_FREE_FIND_CRL_FUNC, CERT_STORE_PROV_FREE_FIND_CTL_FUNC, CERT_STORE_PROV_GET_CERT_PROPERTY_FUNC, CERT_STORE_PROV_GET_CRL_PROPERTY_FUNC, CERT_STORE_PROV_GET_CTL_PROPERTY_FUNC, CERT_STORE_PROV_INFO, CERT_STORE_PROV_INFO structure [Security], CERT_STORE_PROV_LM_SYSTEM_STORE_FLAG, CERT_STORE_PROV_NO_PERSIST_FLAG, CERT_STORE_PROV_READ_CERT_FUNC, CERT_STORE_PROV_READ_CRL_FUNC, CERT_STORE_PROV_READ_CTL_FUNC, CERT_STORE_PROV_SET_CERT_PROPERTY_FUNC, CERT_STORE_PROV_SET_CRL_PROPERTY_FUNC, CERT_STORE_PROV_SET_CTL_PROPERTY_FUNC, CERT_STORE_PROV_SYSTEM_STORE_FLAG, CERT_STORE_PROV_WRITE_CERT_FUNC, CERT_STORE_PROV_WRITE_CRL_FUNC, CERT_STORE_PROV_WRITE_CTL_FUNC, PCERT_STORE_PROV_INFO, PCERT_STORE_PROV_INFO structure pointer [Security], _crypto2_cert_store_prov_info, security.cert_store_prov_info, wincrypt/CERT_STORE_PROV_INFO, wincrypt/PCERT_STORE_PROV_INFO'
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
targetos: Windows
req.typenames: CERT_STORE_PROV_INFO, *PCERT_STORE_PROV_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_STORE_PROV_INFO
 - wincrypt/_CERT_STORE_PROV_INFO
 - PCERT_STORE_PROV_INFO
 - wincrypt/PCERT_STORE_PROV_INFO
 - CERT_STORE_PROV_INFO
 - wincrypt/CERT_STORE_PROV_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_STORE_PROV_INFO
---

# CERT_STORE_PROV_INFO structure


## -description

The <b>CERT_STORE_PROV_INFO</b> structure contains information returned by the installed 
<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a>  function when a store is opened by using the  
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> function.

When opening a store, the  <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a>  function sets all fields in the <b>CERT_STORE_PROV_INFO</b> structure to zero except <b>cbSize</b>, which is set to the size of <b>CERT_STORE_PROV_INFO</b>. The structure is updated by the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a> installable function. If there are no additional callback functions to be called, then <b>cStoreProvFunc</b> remains zero upon return.

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

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_close">CertStoreProvCloseCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_READ_CERT_FUNC"></a><a id="cert_store_prov_read_cert_func"></a><dl>
<dt><b>CERT_STORE_PROV_READ_CERT_FUNC</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_read_cert">CertStoreProvReadCertCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_WRITE_CERT_FUNC"></a><a id="cert_store_prov_write_cert_func"></a><dl>
<dt><b>CERT_STORE_PROV_WRITE_CERT_FUNC</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_write_cert">CertStoreProvWriteCertCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_DELETE_CERT_FUNC"></a><a id="cert_store_prov_delete_cert_func"></a><dl>
<dt><b>CERT_STORE_PROV_DELETE_CERT_FUNC</b></dt>
<dt>3 (0x3)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_cert">CertStoreProvDeleteCertCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_SET_CERT_PROPERTY_FUNC"></a><a id="cert_store_prov_set_cert_property_func"></a><dl>
<dt><b>CERT_STORE_PROV_SET_CERT_PROPERTY_FUNC</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_set_cert_property">CertStoreProvSetCertPropertyCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_READ_CRL_FUNC"></a><a id="cert_store_prov_read_crl_func"></a><dl>
<dt><b>CERT_STORE_PROV_READ_CRL_FUNC</b></dt>
<dt>5 (0x5)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_read_crl">CertStoreProvReadCRLCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_WRITE_CRL_FUNC"></a><a id="cert_store_prov_write_crl_func"></a><dl>
<dt><b>CERT_STORE_PROV_WRITE_CRL_FUNC</b></dt>
<dt>6 (0x6)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_write_crl">CertStoreProvWriteCRLCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_DELETE_CRL_FUNC"></a><a id="cert_store_prov_delete_crl_func"></a><dl>
<dt><b>CERT_STORE_PROV_DELETE_CRL_FUNC</b></dt>
<dt>7 (0x7)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_crl">CertStoreProvDeleteCRLCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_SET_CRL_PROPERTY_FUNC"></a><a id="cert_store_prov_set_crl_property_func"></a><dl>
<dt><b>CERT_STORE_PROV_SET_CRL_PROPERTY_FUNC</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_set_crl_property">CertStoreProvSetCRLPropertyCallback</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_READ_CTL_FUNC"></a><a id="cert_store_prov_read_ctl_func"></a><dl>
<dt><b>CERT_STORE_PROV_READ_CTL_FUNC</b></dt>
<dt>9 (0x9)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_read_ctl">CertStoreProvReadCTL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_WRITE_CTL_FUNC"></a><a id="cert_store_prov_write_ctl_func"></a><dl>
<dt><b>CERT_STORE_PROV_WRITE_CTL_FUNC</b></dt>
<dt>10 (0xA)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_write_ctl">CertStoreProvWriteCTL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_DELETE_CTL_FUNC"></a><a id="cert_store_prov_delete_ctl_func"></a><dl>
<dt><b>CERT_STORE_PROV_DELETE_CTL_FUNC</b></dt>
<dt>11 (0xB)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/SecCrypto/certstoreprovdeletectl">CertStoreProvDeleteCTL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_SET_CTL_PROPERTY_FUNC"></a><a id="cert_store_prov_set_ctl_property_func"></a><dl>
<dt><b>CERT_STORE_PROV_SET_CTL_PROPERTY_FUNC</b></dt>
<dt>12 (0xC)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_set_ctl_property">CertStoreProvSetCTLProperty</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_CONTROL_FUNC"></a><a id="cert_store_prov_control_func"></a><dl>
<dt><b>CERT_STORE_PROV_CONTROL_FUNC</b></dt>
<dt>13 (0xD)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_control">CertStoreProvControl</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FIND_CERT_FUNC"></a><a id="cert_store_prov_find_cert_func"></a><dl>
<dt><b>CERT_STORE_PROV_FIND_CERT_FUNC</b></dt>
<dt>14 (0xE)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/SecCrypto/certstoreprovfindcert">CertStoreProvFindCert</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FREE_FIND_CERT_FUNC"></a><a id="cert_store_prov_free_find_cert_func"></a><dl>
<dt><b>CERT_STORE_PROV_FREE_FIND_CERT_FUNC</b></dt>
<dt>15 (0xF)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/SecCrypto/certstoreprovfreefindcert">CertStoreProvFreeFindCert</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_GET_CERT_PROPERTY_FUNC"></a><a id="cert_store_prov_get_cert_property_func"></a><dl>
<dt><b>CERT_STORE_PROV_GET_CERT_PROPERTY_FUNC</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/SecCrypto/certstoreprovgetcertproperty">CertStoreProvGetCertProperty</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FIND_CRL_FUNC"></a><a id="cert_store_prov_find_crl_func"></a><dl>
<dt><b>CERT_STORE_PROV_FIND_CRL_FUNC</b></dt>
<dt>17 (0x11)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/SecCrypto/certstoreprovfindcrl">CertStoreProvFindCRL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FREE_FIND_CRL_FUNC"></a><a id="cert_store_prov_free_find_crl_func"></a><dl>
<dt><b>CERT_STORE_PROV_FREE_FIND_CRL_FUNC</b></dt>
<dt>18 (0x12)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/SecCrypto/certstoreprovfreefindcrl">CertStoreProvFreeFindCRL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_GET_CRL_PROPERTY_FUNC"></a><a id="cert_store_prov_get_crl_property_func"></a><dl>
<dt><b>CERT_STORE_PROV_GET_CRL_PROPERTY_FUNC</b></dt>
<dt>19 (0x13)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/SecCrypto/certstoreprovgetcrlproperty">CertStoreProvGetCRLProperty</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FIND_CTL_FUNC"></a><a id="cert_store_prov_find_ctl_func"></a><dl>
<dt><b>CERT_STORE_PROV_FIND_CTL_FUNC</b></dt>
<dt>20 (0x14)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/SecCrypto/certstoreprovfindctl">CertStoreProvFindCTL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_FREE_FIND_CTL_FUNC"></a><a id="cert_store_prov_free_find_ctl_func"></a><dl>
<dt><b>CERT_STORE_PROV_FREE_FIND_CTL_FUNC</b></dt>
<dt>21 (0x15)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/SecCrypto/certstoreprovfreefindctl">CertStoreProvFreeFindCTL</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_GET_CTL_PROPERTY_FUNC"></a><a id="cert_store_prov_get_ctl_property_func"></a><dl>
<dt><b>CERT_STORE_PROV_GET_CTL_PROPERTY_FUNC</b></dt>
<dt>22 (0x16)</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/SecCrypto/certstoreprovgetctlproperty">CertStoreProvGetCTLProperty</a>


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
The provider stores <a href="/windows/desktop/SecGloss/c-gly">certificates</a>, <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a>, and <a href="/windows/desktop/SecGloss/c-gly">certificate trust lists</a> that are external to the store's cache.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_PROV_DELETED_FLAG"></a><a id="cert_store_prov_deleted_flag"></a><dl>
<dt><b>CERT_STORE_PROV_DELETED_FLAG</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
The store was successfully deleted. The <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_close">CertStoreProvCloseCallback</a> callback is not called.

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
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetoidfunctionaddress">CryptGetOIDFunctionAddress</a>. 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> calls 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress">CryptFreeOIDFunctionAddress</a> to free a non-null <b>hStoreProvFuncAddr2</b>. This allows the callback to call one other installable function that will be freed when the store is closed.