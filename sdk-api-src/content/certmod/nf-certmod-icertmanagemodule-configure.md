---
UID: NF:certmod.ICertManageModule.Configure
title: ICertManageModule::Configure
author: windows-sdk-content
description: Displays the module user interface.
old-location: security\icertmanagemodule_configure.htm
tech.root: seccrypto
ms.assetid: dc54cda9-1818-40af-9005-f31ad3c110c4
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CCertManageModule object [Security],Configure method, Configure, Configure method [Security], Configure method [Security],CCertManageModule object, Configure method [Security],ICertManageModule interface, ICertManageModule interface [Security],Configure method, ICertManageModule.Configure, ICertManageModule::Configure, _certsrv_icertmanagemodule_configure, certmod/ICertManageModule::Configure, security.icertmanagemodule_configure
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certmod.h
: 
- ICertManageModule.Configure
: 
---

# ICertManageModule::Configure


## -description


The <b>Configure</b> method displays the module user interface.


## -parameters




### -param strConfig [in]

Represents the configuration string for the Certificate Services server in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) as entered for the CA during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa383268(v=VS.85).aspx">ICertConfig</a>.


### -param strStorageLocation [in]

A location that provides storage for the property values, as described in the definition of <i>strStorageLocation</i> in 
<a href="https://msdn.microsoft.com/en-us/library/Aa385031(v=VS.85).aspx">ICertManageModule::GetProperty</a>.


### -param Flags [in]

A value used to determine whether the configuration interface is to be presented to the user. If this value is zero, the user will be presented with an interface for configuring the module. If this value is CMM_REFRESHONLY, Certificate Services will not display the user interface, but the latest changes to the configuration of the module will be in effect when future certificate requests are processed (this allows changes to be incorporated without requiring a response to a user interface).


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



The <b>Configure</b> method displays the module user interface (if one exists), which allows the user to view and change the module's configurable items. A module that implements 
<a href="https://msdn.microsoft.com/en-us/library/Aa385029(v=VS.85).aspx">ICertManageModule</a> can have its <b>Configure</b> method called when the Certificate Services Manager Policy or Exit Module property page is active and the user chooses the <b>Configure</b> button. The Certificate Services Manager will pass the location referenced by <i>strStorageLocation</i> to this module, and the implementation of this method can then use this location as needed. Note that it is possible that a module may not have configurable items (hence, a user interface would not be necessary), but it would still be necessary to implement this method. The example below does not allow a user to make a configuration change, but it does implement this method.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;Certmod.h&gt;

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
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383268(v=VS.85).aspx">ICertConfig</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385029(v=VS.85).aspx">ICertManageModule</a>
 

 

