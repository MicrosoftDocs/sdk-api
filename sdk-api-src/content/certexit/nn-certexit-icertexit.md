---
UID: NN:certexit.ICertExit
title: ICertExit (certexit.h)
description: Provides communications between the Certificate Services server and an exit module.
helpviewer_keywords: ["ICertExit","ICertExit interface [Security]","ICertExit interface [Security]","described","_certsrv_icertexit","certexit/ICertExit","security.icertexit"]
old-location: security\icertexit.htm
tech.root: security
ms.assetid: 731c4f3c-20b4-4f3d-8241-a94cdf656fe5
ms.date: 12/05/2018
ms.keywords: ICertExit, ICertExit interface [Security], ICertExit interface [Security],described, _certsrv_icertexit, certexit/ICertExit, security.icertexit
req.header: certexit.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertExit
 - certexit/ICertExit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certexit.h
api_name:
 - ICertExit
---

# ICertExit interface


## -description

The <b>ICertExit</b> interface  provides communications between  the Certificate Services server and an exit module.
<div class="alert"><b>Note</b>  The exit module can communicate with the Certificate Services server by using the <a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a> interface.</div><div> </div>The Certificate Services server calls the <b>ICertExit</b> methods to perform the following tasks:<ul>
<li>Initialize the Certificate Services server.</li>
<li>Notify the exit module of an event such as certificate issuance, <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) issuance, or server shutdown, has occurred.</li>
<li>Retrieve a description of the exit module.</li>
</ul>


<b>ICertExit</b> is defined in Certexit.h. When you create your program, however, use Certsrv.h as the include file.

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertExit</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertExit</b> also has these types of members:

## -remarks

Implementers of <b>ICertExit</b> should also implement 
<a href="/windows/desktop/api/certmod/nn-certmod-icertmanagemodule">ICertManageModule</a>. Additionally, the ProgID for a class implementing <b>ICertExit</b> must conform to a naming convention. Specifically, the ProgID must be of the form:

<b>"</b><i>MyApp</i><b>.Exit"</b>

Where <i>MyApp</i> is a specifier that identifies the application. For example, in C++, the following code could be used in the DECLARE_REGISTRY macro of a class (CMyCertExitModule) which implements <b>ICertExit</b>.


```cpp
DECLARE_REGISTRY(
    CMyCertExitModule,
    L"MyCode.Exit.1",
    L"MyCode.Exit",
    IDS_CERTEXITMODULE_DESC,
    THREADFLAGS_BOTH)
```


For the previous sample, the IDS_CERTEXITMODULE_DESC value is an application-specific identifier in the resource file (.rc) for a string that describes the class.

String constants defined in Certmod.h can be used to simplify following the naming convention.

<table>
<tr>
<th>Constant</th>
<th>Value</th>
</tr>
<tr>
<td>
<b>wszCERTEXITMODULE_POSTFIX</b>

</td>
<td>
TEXT(".Exit")

</td>
</tr>
</table>
 

No more than one Visual Basic Scripting Edition exit module may be registered on the Certificate Services server at one time. If more than one Visual Basic Scripting Edition exit module is registered, the Certification Authority MMC snap-in, Certificate Services application, or certutil command line program may produce errors. Note that the Visual Basic Scripting Edition development environment automatically registers a DLL when it is successfully built. As a result, you may encounter this situation when one Visual Basic Scripting Edition exit module is already registered and another Visual Basic Scripting Edition exit module is created. To avoid this situation, you must unregister one of the Visual Basic Scripting Edition exit modules, by means of the command-line instruction <b>regsvr32 /u </b><i>FileName</i><b>.dll</b>, where <i>FileName</i>.dll is the name of the Visual Basic Scripting Edition exit module that is not intended to be made active.

Implementers of <b>ICertExit</b> in Visual Basic Scripting Edition must name their project in the form:

<b>"</b><i>MyApp</i><b>"</b>

Where <i>MyApp</i> is a specifier that identifies the application; further, the class implementing <b>ICertExit</b> must be named <b>"Exit"</b>.

## -see-also

<a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
