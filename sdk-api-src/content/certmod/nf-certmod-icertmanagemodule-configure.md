---
UID: NF:certmod.ICertManageModule.Configure
title: ICertManageModule::Configure (certmod.h)
description: Displays the module user interface.
helpviewer_keywords: ["CCertManageModule object [Security]","Configure method","Configure","Configure method [Security]","Configure method [Security]","CCertManageModule object","Configure method [Security]","ICertManageModule interface","ICertManageModule interface [Security]","Configure method","ICertManageModule.Configure","ICertManageModule::Configure","_certsrv_icertmanagemodule_configure","certmod/ICertManageModule::Configure","security.icertmanagemodule_configure"]
old-location: security\icertmanagemodule_configure.htm
tech.root: security
ms.assetid: dc54cda9-1818-40af-9005-f31ad3c110c4
ms.date: 12/05/2018
ms.keywords: CCertManageModule object [Security],Configure method, Configure, Configure method [Security], Configure method [Security],CCertManageModule object, Configure method [Security],ICertManageModule interface, ICertManageModule interface [Security],Configure method, ICertManageModule.Configure, ICertManageModule::Configure, _certsrv_icertmanagemodule_configure, certmod/ICertManageModule::Configure, security.icertmanagemodule_configure
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
 - ICertManageModule::Configure
 - certmod/ICertManageModule::Configure
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
 - ICertManageModule.Configure
 - CCertManageModule.Configure
---

# ICertManageModule::Configure


## -description

The <b>Configure</b> method displays the module user interface.

## -parameters

### -param strConfig [in]

Represents the configuration string for the Certificate Services server in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) as entered for the CA during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

### -param strStorageLocation [in]

A location that provides storage for the property values, as described in the definition of <i>strStorageLocation</i> in 
<a href="/windows/desktop/api/certmod/nf-certmod-icertmanagemodule-getproperty">ICertManageModule::GetProperty</a>.

### -param Flags [in]

A value used to determine whether the configuration interface is to be presented to the user. If this value is zero, the user will be presented with an interface for configuring the module. If this value is CMM_REFRESHONLY, Certificate Services will not display the user interface, but the latest changes to the configuration of the module will be in effect when future certificate requests are processed (this allows changes to be incorporated without requiring a response to a user interface).

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <b>Configure</b> method displays the module user interface (if one exists), which allows the user to view and change the module's configurable items. A module that implements 
<a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a> can have its <b>Configure</b> method called when the Certificate Services Manager Policy or Exit Module property page is active and the user chooses the <b>Configure</b> button. The Certificate Services Manager will pass the location referenced by <i>strStorageLocation</i> to this module, and the implementation of this method can then use this location as needed. Note that it is possible that a module may not have configurable items (hence, a user interface would not be necessary), but it would still be necessary to implement this method. The example below does not allow a user to make a configuration change, but it does implement this method.


#### Examples


```cpp
#include <windows.h>
#include <Certmod.h>

HRESULT CCertManagePolicyModule::Configure( 
            /* [in] */ const BSTR strConfig,
            /* [in] */ BSTR strStorageLocation,
            /* [in] */ LONG Flags)
{
    if ( CMM_REFRESHONLY != Flags )
        MessageBox(NULL,
                   L"This module has no configurable items",
                   L"MyModule",
                   (MB_OK|MB_ICONINFORMATION));

    return S_OK;
}
```

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>



<a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a>