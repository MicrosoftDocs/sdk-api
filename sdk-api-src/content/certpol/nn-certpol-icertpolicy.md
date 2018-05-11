---
UID: NN:certpol.ICertPolicy
title: ICertPolicy
author: windows-driver-content
description: Provides communications between the Certificate Services server engine and the policy module.
old-location: security\icertpolicy.htm
old-project: SecCrypto
ms.assetid: 14031490-be8e-47f9-8c66-ae27f7d3599c
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ICertPolicy, ICertPolicy interface [Security], ICertPolicy interface [Security],described, _certsrv_icertpolicy, certpol/ICertPolicy, security.icertpolicy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certidl.lib
-	Certidl.dll
api_name:
-	ICertPolicy
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: 
req.irql: 
---

# ICertPolicy interface


## -description


The <b>ICertPolicy</b> interface  provides communications between the Certificate Services server engine and the policy module.
<div class="alert"><b>Note</b>  The policy module can communicate with the Certificate Services server engine by using the <a href="https://msdn.microsoft.com/7d16161e-9827-46a0-9989-30ebca792bb1">ICertServerPolicy</a> interface.</div><div> </div>The Certificate Services server engine calls the <b>ICertPolicy</b> methods to perform the following tasks:<ul>
<li>Initialize the policy module.</li>
<li>Notify the policy module that a new request has entered the system. The policy module can then use the methods of the <a href="https://msdn.microsoft.com/7d16161e-9827-46a0-9989-30ebca792bb1">ICertServerPolicy</a> interface to indicate that the request is good and should be issued, is bad and should be denied, or should be held for later consideration.</li>
<li>Retrieve a description of the policy module and its functionality.</li>
<li>Notify the policy module that the Certificate Services server is being terminated.</li>
</ul>


Policy modules should implement both <b>ICertPolicy</b> and 
<a href="https://msdn.microsoft.com/82b7b770-c098-40da-8a4e-8eb0e0b8a645">ICertManageModule</a>.

<b>ICertPolicy</b> is defined in Certpol.h. When you create your program, however, use Certsrv.h as the include file.

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPolicy</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICertPolicy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertPolicy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546575">GetDescription</a>
</td>
<td align="left" width="63%">
Returns a human-readable description of the policy module and its function.</p> (Inherited from <b>ICertPolicy</b><a href="https://msdn.microsoft.com/2e48b096-e23a-4106-bfaf-f089d2291fba">CCertPolicy</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Called by the server engine to allow the policy module to perform initialization tasks.</p> (Inherited from <b>ICertPolicy</b><a href="https://msdn.microsoft.com/2e48b096-e23a-4106-bfaf-f089d2291fba">CCertPolicy</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a>
</td>
<td align="left" width="63%">
Called by the server engine before the server is terminated.</p> (Inherited from <b>ICertPolicy</b><a href="https://msdn.microsoft.com/2e48b096-e23a-4106-bfaf-f089d2291fba">CCertPolicy</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/860f0eb0-5b23-44bd-8416-687a94962f1b">VerifyRequest</a>
</td>
<td align="left" width="63%">
Notifies the policy module that a new request has entered the system.</p> (Inherited from <b>ICertPolicy</b><a href="https://msdn.microsoft.com/2e48b096-e23a-4106-bfaf-f089d2291fba">CCertPolicy</a>)</td>
</tr>
</table> 


## -remarks



Only a stand-alone <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> should use custom policy or exit modules; when running an enterprise certification authority, the use of Microsoft-provided policy and exit modules is strongly recommended.

Implementers of <b>ICertPolicy</b> should also implement 
<a href="https://msdn.microsoft.com/82b7b770-c098-40da-8a4e-8eb0e0b8a645">ICertManageModule</a>. Additionally, the ProgID for a class implementing <b>ICertPolicy</b> must conform to a naming convention. Specifically, the ProgID must be of the form:

<b>"</b><i>MyApp</i><b>.Policy"</b>

Where <i>MyApp</i> is a specifier that identifies the application. For example, in C++, the following code could be used in the DECLARE_REGISTRY macro of a class (CMyCertPolicyModule) which implements <b>ICertPolicy</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DECLARE_REGISTRY(
    CMyCertPolicyModule,
    L"MyCode.Policy.1",
    L"MyCode.Policy",
    IDS_CERTPOLICYMODULE_DESC,
    THREADFLAGS_BOTH);</pre>
</td>
</tr>
</table></span></div>
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



