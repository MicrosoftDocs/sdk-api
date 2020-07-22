---
UID: NN:certmod.ICertManageModule
title: ICertManageModule (certmod.h)
description: Provided to retrieve information about a Certificate Services Policy or Exit module.
helpviewer_keywords: ["ICertManageModule","ICertManageModule interface [Security]","ICertManageModule interface [Security]","described","_certsrv_icertmanagemodule","certmod/ICertManageModule","security.icertmanagemodule"]
old-location: security\icertmanagemodule.htm
tech.root: security
ms.assetid: 82b7b770-c098-40da-8a4e-8eb0e0b8a645
ms.date: 12/05/2018
ms.keywords: ICertManageModule, ICertManageModule interface [Security], ICertManageModule interface [Security],described, _certsrv_icertmanagemodule, certmod/ICertManageModule, security.icertmanagemodule
f1_keywords:
- certmod/ICertManageModule
dev_langs:
- c++
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
- ICertManageModule
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertManageModule interface


## -description


The <b>ICertManageModule</b> interface is provided to retrieve information about a Certificate Services 
<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/policy-modules">Policy</a> or 
<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/exit-modules">Exit</a> module.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertManageModule</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertManageModule</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertManageModule</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certmod/nf-certmod-icertmanagemodule-configure">Configure</a>
</td>
<td align="left" width="63%">
Invokes module configuration user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certmod/nf-certmod-icertmanagemodule-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property in the module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certmod/nf-certmod-icertmanagemodule-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Assigns a value to a property in the module.

</td>
</tr>
</table> 


## -remarks



The <b>ICertManageModule</b> interface provides a method to invoke the module user interface for setting and viewing configuration settings. Writers of Policy and Exit modules should implement the <b>ICertManageModule</b> interface (in addition to the <a href="https://docs.microsoft.com/windows/desktop/api/certpol/nn-certpol-icertpolicy">ICertPolicy</a> and <a href="https://docs.microsoft.com/windows/desktop/api/certexit/nn-certexit-icertexit">ICertExit</a> interfaces, respectively). An enterprise <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) should always use the Microsoft-provided enterprise policy and exit modules; additional exit modules are permitted for enterprise CAs.

The following is an example of what could be used in the DECLARE_REGISTRY macro of a class (CMyCertManagePolicyModule) which implements <b>ICertManageModule</b>.


```cpp
DECLARE_REGISTRY(
    CMyCertManagePolicyModule,
    L"MyCode.PolicyManage.1",
    L"MyCode.PolicyManage",
    IDS_CERTMANAGEPOLICYMODULE_DESC,
    THREADFLAGS_BOTH);
```


The IDS_CERTMANAGEPOLICYMODULE_DESC value is an application-specific identifier that identifies a string table string in the resource file (.rc) which describes the class.
			
			
			
			

<b>ICertManageModule</b> is defined in Certmod.h. When you create your program, however, use Certsrv.h as the include file.

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

In Visual Basic Scripting Edition, the name of the class that implements <b>ICertManageModule</b> must be either "PolicyManage" or "PolicyExit", depending on the type of module being created. The following string constants defined in Certmod.h may be used to simplify following the naming convention.

<table>
<tr>
<th>Constant</th>
<th>Value</th>
</tr>
<tr>
<td>
<b>wszCERTMANAGEEXIT_POSTFIX</b>

</td>
<td>
TEXT(".ExitManage")

</td>
</tr>
<tr>
<td>
<b>wszCERTMANAGEPOLICY_POSTFIX</b>

</td>
<td>
TEXT(".PolicyManage")

</td>
</tr>
</table>
 



