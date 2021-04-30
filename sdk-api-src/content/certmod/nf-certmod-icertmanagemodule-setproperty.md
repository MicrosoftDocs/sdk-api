---
UID: NF:certmod.ICertManageModule.SetProperty
title: ICertManageModule::SetProperty (certmod.h)
description: Allows a module to set a property value.
helpviewer_keywords: ["CCertManageModule object [Security]","SetProperty method","Copyright","Description","File Version","ICertManageModule interface [Security]","SetProperty method","ICertManageModule.SetProperty","ICertManageModule::SetProperty","Name","Product Version","SetProperty","SetProperty method [Security]","SetProperty method [Security]","CCertManageModule object","SetProperty method [Security]","ICertManageModule interface","_certsrv_icertmanagemodule_setproperty","certmod/ICertManageModule::SetProperty","security.icertmanagemodule_setproperty"]
old-location: security\icertmanagemodule_setproperty.htm
tech.root: security
ms.assetid: 582ace4a-da88-41b7-86dd-d6a74fc9e97a
ms.date: 12/05/2018
ms.keywords: CCertManageModule object [Security],SetProperty method, Copyright, Description, File Version, ICertManageModule interface [Security],SetProperty method, ICertManageModule.SetProperty, ICertManageModule::SetProperty, Name, Product Version, SetProperty, SetProperty method [Security], SetProperty method [Security],CCertManageModule object, SetProperty method [Security],ICertManageModule interface, _certsrv_icertmanagemodule_setproperty, certmod/ICertManageModule::SetProperty, security.icertmanagemodule_setproperty
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
 - ICertManageModule::SetProperty
 - certmod/ICertManageModule::SetProperty
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
 - ICertManageModule.SetProperty
 - CCertManageModule.SetProperty
---

# ICertManageModule::SetProperty


## -description

The <b>SetProperty</b> method allows a module to set a property value.

## -parameters

### -param strConfig [in]

Represents the configuration string for the Certificate Services server in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) as entered for the CA during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

### -param strStorageLocation [in]

The location that provides storage for the property values, as described in the definition of <i>strStorageLocation</i> in 
<a href="/windows/desktop/api/certmod/nf-certmod-icertmanagemodule-getproperty">ICertManageModule::GetProperty</a>.

### -param strPropertyName [in]

The name of the property whose value is being assigned. Policy and exit modules should support the following properties, which are used by Certificate Services Manager.

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

### -param pvarProperty [in]

A value that is being assigned to the property specified by <i>strPropertyName</i>.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This method is intended for future functionality. A minimal implementation is required, however, to meet the requirements of the <a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a> interface.


#### Examples


```cpp
#include <windows.h>
#include <Certmod.h>

HRESULT CCertManagePolicyModule::SetProperty(
            /* [in] */ const BSTR strConfig,
            /* [in] */ BSTR strStorageLocation,
            /* [in] */ BSTR strPropertyName,
            /* [in] */ LONG Flags,
            /* [in] */ const VARIANT *pvarProperty)
{
    // This implementation fulfills the minimal requirement
    // needed for ICertManageModule::SetProperty.
    return S_OK;
}
```

## -see-also

<b>CCertManageModule</b>



<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>



<a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a>



<a href="/windows/desktop/api/certmod/nf-certmod-icertmanagemodule-getproperty">ICertManageModule::GetProperty</a>