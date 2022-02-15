---
UID: NN:certpol.ICertPolicy2
title: ICertPolicy2 (certpol.h)
description: Provide communications between the Certificate Services server engine and the policy module.
helpviewer_keywords: ["ICertPolicy2","ICertPolicy2 interface [Security]","ICertPolicy2 interface [Security]","described","_certsrv_icertpolicy2","certpol/ICertPolicy2","security.icertpolicy2"]
old-location: security\icertpolicy2.htm
tech.root: security
ms.assetid: 2e48b096-e23a-4106-bfaf-f089d2291fba
ms.date: 12/05/2018
ms.keywords: ICertPolicy2, ICertPolicy2 interface [Security], ICertPolicy2 interface [Security],described, _certsrv_icertpolicy2, certpol/ICertPolicy2, security.icertpolicy2
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
 - ICertPolicy2
 - certpol/ICertPolicy2
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
 - ICertPolicy2
---

# ICertPolicy2 interface


## -description

The <b>ICertPolicy2</b> interface is one of two interfaces that   provide communications between the Certificate Services server engine and the policy module.
<div class="alert"><b>Note</b>  The policy module can communicate with the Certificate Services server engine by using the <a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a> interface.</div><div> </div>The Certificate Services server engine calls the <b>ICertPolicy2</b> methods to perform the following tasks:<ul>
<li>Initialize the policy module.</li>
<li>Notify the policy module that a new request has entered the system. The policy module can then use the methods of the <a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a> interface to indicate that the request is good and should be issued, is bad and should be denied, or should be held for later consideration.</li>
<li>Retrieve a description of the policy module and its functionality.</li>
<li>Notify the policy module that the Certificate Services server is being terminated.</li>
</ul>


Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertPolicy2</b> interface inherits from <a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy">ICertPolicy</a> and <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>. <b>ICertPolicy2</b> also has these types of members:

## -remarks

Implementers of <a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy">ICertPolicy</a> should also implement 
<a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a>. Additionally, the ProgID for a class implementing <b>ICertPolicy</b> must conform to a naming convention. Specifically, the ProgID must be of the form:

<b>"</b><i>MyApp</i><b>.Policy"</b>

Where <i>MyApp</i> is a specifier that identifies the application. For example, in C++, the following could be used in the DECLARE_REGISTRY macro of a class (CMyCertPolicyModule) which implements <a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy">ICertPolicy</a>.


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
<td><b>wszCERTPOLICYMODULE_POSTFIX</b></td>
<td>TEXT(".Policy")</td>
</tr>
</table>
 

No more than one Visual Basic Scripting Edition policy module may be registered on the Certificate Services server at one time. If more than one such policy module is registered on the Certificate Services server, the Certification Authority MMC snap-in, Certificate Services application, or Certutil tool may produce errors. Note that the  Visual Basic Scripting Edition development environment automatically registers a DLL when it is successfully built. As a result, you may encounter this situation when one Visual Basic Scripting Edition policy module is already registered and another Visual Basic Scripting Edition policy module is created. To avoid this situation, you must unregister one of the Visual Basic Scripting Edition policy modules, by using the command-line instruction <b>regsvr32 /u </b><i>FileName.dll</i>, where <i>FileName.dll</i> is the name of the Visual Basic Scripting Edition policy module that you do not intend to make active.

Implementers of <a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy">ICertPolicy</a> in Visual Basic Scripting Edition must name their project in the form:

<b>"</b><i>MyApp</i><b>"</b>

Where <i>MyApp</i> is a specifier that identifies the application; further, the class implementing <a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy">ICertPolicy</a> must be named <b>"Policy"</b>.
