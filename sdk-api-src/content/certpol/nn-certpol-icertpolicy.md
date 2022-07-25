---
UID: NN:certpol.ICertPolicy
title: ICertPolicy (certpol.h)
description: Provides communications between the Certificate Services server engine and the policy module.
helpviewer_keywords: ["ICertPolicy","ICertPolicy interface [Security]","ICertPolicy interface [Security]","described","_certsrv_icertpolicy","certpol/ICertPolicy","security.icertpolicy"]
old-location: security\icertpolicy.htm
tech.root: security
ms.assetid: 14031490-be8e-47f9-8c66-ae27f7d3599c
ms.date: 12/05/2018
ms.keywords: ICertPolicy, ICertPolicy interface [Security], ICertPolicy interface [Security],described, _certsrv_icertpolicy, certpol/ICertPolicy, security.icertpolicy
req.header: certpol.h
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
 - ICertPolicy
 - certpol/ICertPolicy
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
 - ICertPolicy
---

# ICertPolicy interface


## -description

The <b>ICertPolicy</b> interface  provides communications between the Certificate Services server engine and the policy module.
<div class="alert"><b>Note</b>  The policy module can communicate with the Certificate Services server engine by using the <a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a> interface.</div><div> </div>The Certificate Services server engine calls the <b>ICertPolicy</b> methods to perform the following tasks:<ul>
<li>Initialize the policy module.</li>
<li>Notify the policy module that a new request has entered the system. The policy module can then use the methods of the <a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a> interface to indicate that the request is good and should be issued, is bad and should be denied, or should be held for later consideration.</li>
<li>Retrieve a description of the policy module and its functionality.</li>
<li>Notify the policy module that the Certificate Services server is being terminated.</li>
</ul>


Policy modules should implement both <b>ICertPolicy</b> and 
<a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a>.

<b>ICertPolicy</b> is defined in Certpol.h. When you create your program, however, use Certsrv.h as the include file.

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertPolicy</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertPolicy</b> also has these types of members:

## -remarks

Only a stand-alone <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> should use custom policy or exit modules; when running an enterprise certification authority, the use of Microsoft-provided policy and exit modules is strongly recommended.

Implementers of <b>ICertPolicy</b> should also implement 
<a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a>. Additionally, the ProgID for a class implementing <b>ICertPolicy</b> must conform to a naming convention. Specifically, the ProgID must be of the form:

<b>"</b><i>MyApp</i><b>.Policy"</b>

Where <i>MyApp</i> is a specifier that identifies the application. For example, in C++, the following code could be used in the DECLARE_REGISTRY macro of a class (CMyCertPolicyModule) which implements <b>ICertPolicy</b>.


```cpp
DECLARE_REGISTRY(
    CMyCertPolicyModule,
    L"MyCode.Policy.1",
    L"MyCode.Policy",
    IDS_CERTPOLICYMODULE_DESC,
    THREADFLAGS_BOTH);
```


For the previous example, the IDS_CERTPOLICYMODULE_DESC value is an application-specific identifier in the resource file (.rc) for a string which describes the class.

String constants defined in Certmod.h can be used to simplify following the naming convention.

<table>
<tr>
<th>Constant</th>
<th>Value</th>
</tr>
<tr>
<td>
<b>wszCERTPOLICYMODULE_POSTFIX</b>

</td>
<td>
TEXT(".Policy")

</td>
</tr>
</table>
 

No more than one Visual Basic Scripting Edition policy module may be registered on the Certificate Services server at one time. If more than one such policy module is registered on the Certificate Services server, the Certification Authority MMC snap-in, Certificate Services application, or certutil command line program may produce errors. Note that  the Visual Basic Scripting Edition development environment automatically registers a DLL when it is successfully built. As a result, you may encounter this situation when one Visual Basic Scripting Edition policy module is already registered and another Visual Basic Scripting Edition policy module is created. To avoid this situation, you must unregister one of the Visual Basic Scripting Edition policy modules, by using the command-line instruction <b>regsvr32 /u </b><i>FileName.dll</i>, where <i>FileName.dll</i> is the name of the Visual Basic Scripting Edition policy module that you do not intend to make active.

Implementers of <b>ICertPolicy</b> in Visual Basic Scripting Edition must name their project in the form: 

<b>"</b><i>MyApp</i><b>"</b>

Where <i>MyApp</i> is a specifier that identifies the application; further, the class implementing <b>ICertPolicy</b> must be named <b>"Policy"</b>.
