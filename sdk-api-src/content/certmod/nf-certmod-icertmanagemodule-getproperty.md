---
UID: NF:certmod.ICertManageModule.GetProperty
title: ICertManageModule::GetProperty (certmod.h)
description: Retrieves a module's property value.
helpviewer_keywords: ["CCertManageModule object [Security]","GetProperty method","Copyright","Description","File Version","GetProperty","GetProperty method [Security]","GetProperty method [Security]","CCertManageModule object","GetProperty method [Security]","ICertManageModule interface","ICertManageModule interface [Security]","GetProperty method","ICertManageModule.GetProperty","ICertManageModule::GetProperty","Name","Product Version","_certsrv_icertmanagemodule_getproperty","certmod/ICertManageModule::GetProperty","security.icertmanagemodule_getproperty"]
old-location: security\icertmanagemodule_getproperty.htm
tech.root: security
ms.assetid: f01bfcec-7031-4283-a847-0d59929e4ee5
ms.date: 12/05/2018
ms.keywords: CCertManageModule object [Security],GetProperty method, Copyright, Description, File Version, GetProperty, GetProperty method [Security], GetProperty method [Security],CCertManageModule object, GetProperty method [Security],ICertManageModule interface, ICertManageModule interface [Security],GetProperty method, ICertManageModule.GetProperty, ICertManageModule::GetProperty, Name, Product Version, _certsrv_icertmanagemodule_getproperty, certmod/ICertManageModule::GetProperty, security.icertmanagemodule_getproperty
req.header: certmod.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertManageModule::GetProperty
 - certmod/ICertManageModule::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certidl.lib
 - Certidl.dll
api_name:
 - ICertManageModule.GetProperty
 - CCertManageModule.GetProperty
---

# ICertManageModule::GetProperty


## -description

The <b>GetProperty</b> method retrieves a module's property value.

## -parameters

### -param strConfig [in]

Represents the configuration string for the Certificate Services server in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) as entered for the CA during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

### -param strStorageLocation [in]

A registry key that denotes the storage location in the <b>HKEY_LOCAL_MACHINE</b> hive for the property values. This value is in the following form:


<pre><b>SYSTEM</b>
   <b>CurrentControlSet</b>
      <b>Services</b>
         <b>CertSvc</b>
            <b>Configuration</b>
               <i>CAName</i>
                  <i>PolicyOrExitModules</i>
                     <i>MyModule.PolicyOrExit</i></pre>


The <i>CAName</i> is the name of the certification authority's configuration string, <i>PolicyOrExitModules</i> will be either "Policy" or "Exit" (depending on whether a Policy or Exit module applies to this implementation of <b>ICertManageModule</b>), and <i>MyModule.PolicyOrExit</i> is the application-specific identifier for the module. Note that <i>CAName</i> is the <a href="/windows/desktop/SecGloss/s-gly">sanitized name</a> for the certification authority. For information about the sanitized name, see 
<a href="/windows/desktop/api/certcli/nf-certcli-icertconfig-getconfig">ICertConfig::GetConfig</a>. The use of this storage location is for future use.

### -param strPropertyName [in]

The name of the property being queried. Policy and exit modules should support the following properties. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Name"></a><a id="name"></a><a id="NAME"></a><dl>
<dt><b>Name</b></dt>
</dl>
</td>
<td width="60%">
Name of the module.

</td>
</tr>
<tr>
<td width="40%"><a id="Description"></a><a id="description"></a><a id="DESCRIPTION"></a><dl>
<dt><b>Description</b></dt>
</dl>
</td>
<td width="60%">
Description of the module.

</td>
</tr>
<tr>
<td width="40%"><a id="Copyright"></a><a id="copyright"></a><a id="COPYRIGHT"></a><dl>
<dt><b>Copyright</b></dt>
</dl>
</td>
<td width="60%">
Copyright pertaining to the module.

</td>
</tr>
<tr>
<td width="40%"><a id="File_Version"></a><a id="file_version"></a><a id="FILE_VERSION"></a><dl>
<dt><b>File Version</b></dt>
</dl>
</td>
<td width="60%">
Version of the module file.

</td>
</tr>
<tr>
<td width="40%"><a id="Product_Version"></a><a id="product_version"></a><a id="PRODUCT_VERSION"></a><dl>
<dt><b>Product Version</b></dt>
</dl>
</td>
<td width="60%">
Version of the module.

</td>
</tr>
</table>

### -param Flags [in]

This parameter is reserved and must be set to zero.

### -param pvarProperty [out, retval]

A pointer to a <b>VARIANT</b> that is the retrieved value for the property specified by <i>strPropertyName</i>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>Variant</b> that represents the value of the property named <i>strPropertyName</i>.

## -remarks

Implementing <b>ICertManageModule</b> allows the Certificate Services Manager to retrieve the module's properties by calling <b>GetProperty</b>. The properties can then be displayed in Certificate Services Manager property pages for Policy and Exit Modules. The Certificate Services Manager will pass the location referenced by <i>strStorageLocation</i> to this module, and in future versions the implementation of this method can then use this location as needed. The following example does not use <i>strStorageLocation</i> but instead, maintains the property values in memory.


#### Examples


```cpp
#include <windows.h>
#include <Certmod.h>

HRESULT CCertManagePolicyModule::GetProperty(
            /* [in] */ const BSTR strConfig,
            /* [in] */ BSTR strStorageLocation,
            /* [in] */ BSTR strPropertyName,
            /* [in] */ LONG Flags,
            /* [retval][out] */ VARIANT *pvarProperty)
{
    // Array of property Names.
    // These values are defined in Certmod.h.
    wchar_t const * awszPropName[] =
    {
        wszCMM_PROP_NAME,
        wszCMM_PROP_DESCRIPTION,
        wszCMM_PROP_COPYRIGHT,
        wszCMM_PROP_FILEVER,
        wszCMM_PROP_PRODUCTVER
    };

    // Array of property Values.
    // These values are module-specific, and
    // correspond to the property names in    
    // awszPropName (same index).
    wchar_t const * awszPropValue[] = 
   {
        L"MyModule",                      // NAME
        L"Description of MyModule",       // DESCRIPTION
        L"Copyright 1998",                // COPYRIGHT
        L"1.0",                           // FILE VERSION
        L"1.0"                            // PRODUCT VERSION
    };
    int     i;
    bool    bFound = FALSE;
    HRESULT hr;

    // Return appropriate error if strPropertyName is NULL.
    if (NULL == strPropertyName)
        return E_INVALIDARG;

    // Return appropriate error if pvarProperty is NULL.
    if (NULL == pvarProperty)
        return E_POINTER;
    // Determine whether the requested property is in the Name array.
    for (i=0; i<sizeof(awszPropName)/sizeof(wchar_t *); i++)
        if (!wcscmp( strPropertyName, awszPropName[i]))        
        {
            bFound = TRUE;  // Found the index for the property.
            break;
        }
    if ( !bFound )
        return S_FALSE;     // Requested property not found.

    // Allocate storage for the property value.
    pvarProperty->bstrVal = SysAllocString(awszPropValue[i]);
    if (NULL == pvarProperty->bstrVal)
        return E_OUTOFMEMORY;   

    pvarProperty->vt = VT_BSTR;

    return S_OK;
}
```

## -see-also

<b>CCertManageModule</b>



<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>



<a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a>



<a href="/windows/desktop/api/certmod/nf-certmod-icertmanagemodule-setproperty">ICertManageModule::SetProperty</a>
