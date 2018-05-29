---
UID: NN:certmod.ICertManageModule
title: ICertManageModule
author: windows-sdk-content
description: Provided to retrieve information about a Certificate Services Policy or Exit module.
old-location: security\icertmanagemodule.htm
old-project: SecCrypto
ms.assetid: 82b7b770-c098-40da-8a4e-8eb0e0b8a645
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: ICertManageModule, ICertManageModule interface [Security], ICertManageModule interface [Security],described, _certsrv_icertmanagemodule, certmod/ICertManageModule, security.icertmanagemodule
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
-	ICertManageModule
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: 
req.irql: 
---

# ICertManageModule interface


## -description


The <b>ICertManageModule</b> interface is provided to retrieve information about a Certificate Services 
<a href="https://msdn.microsoft.com/23d920ea-af62-42ce-ad48-c7a03ab55fc9">Policy</a> or 
<a href="https://msdn.microsoft.com/5e7ee1f4-7e07-4a08-8e72-89b449804bc2">Exit</a> module.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertManageModule</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICertManageModule</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/dc54cda9-1818-40af-9005-f31ad3c110c4">Configure</a>
</td>
<td align="left" width="63%">
Invokes module configuration user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f01bfcec-7031-4283-a847-0d59929e4ee5">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property in the module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/582ace4a-da88-41b7-86dd-d6a74fc9e97a">SetProperty</a>
</td>
<td align="left" width="63%">
Assigns a value to a property in the module.

</td>
</tr>
</table> 


## -remarks



The <b>ICertManageModule</b> interface provides a method to invoke the module user interface for setting and viewing configuration settings. Writers of Policy and Exit modules should implement the <b>ICertManageModule</b> interface (in addition to the <a href="https://msdn.microsoft.com/14031490-be8e-47f9-8c66-ae27f7d3599c">ICertPolicy</a> and <a href="https://msdn.microsoft.com/731c4f3c-20b4-4f3d-8241-a94cdf656fe5">ICertExit</a> interfaces, respectively). An enterprise <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) should always use the Microsoft-provided enterprise policy and exit modules; additional exit modules are permitted for enterprise CAs.

The following is an example of what could be used in the DECLARE_REGISTRY macro of a class (CMyCertManagePolicyModule) which implements <b>ICertManageModule</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DECLARE_REGISTRY(
    CMyCertManagePolicyModule,
    L"MyCode.PolicyManage.1",
    L"MyCode.PolicyManage",
    IDS_CERTMANAGEPOLICYMODULE_DESC,
    THREADFLAGS_BOTH);</pre>
</td>
</tr>
</table></span></div>
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
 



