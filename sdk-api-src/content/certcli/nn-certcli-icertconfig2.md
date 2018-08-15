---
UID: NN:certcli.ICertConfig2
title: ICertConfig2
author: windows-sdk-content
description: Provide functionality for retrieving the public configuration data (specified during client setup) for a Certificate Services server.
old-location: security\icertconfig2.htm
old-project: seccrypto
ms.assetid: 6bac5961-f9cc-4859-affa-aa7ed152ebfa
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICertConfig2, ICertConfig2 interface [Security], ICertConfig2 interface [Security],described, _certsrv_icertconfig2, certcli/ICertConfig2, security.icertconfig2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certcli.h
req.include-header: Certsrv.h
req.redist: 
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
tech.root: 
req.typenames: X509EnrollmentAuthFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertConfig2
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
---

# ICertConfig2 interface


## -description


The <b>ICertConfig2</b> interface is one of two interfaces that  provide functionality for retrieving  the public  configuration data (specified during client setup) for a Certificate Services server.

The <b>ICertConfig2</b> interface is used to perform the following tasks:<ul>
<li>Enumerate through the  configuration strings for a Certificate Services server.</li>
<li>Retrieve the  default  configuration for a Certificate Services server.</li>
<li>Retrieve the  details of a specific Certificate Services server configuration.</li>
<li>Reset the configuration of a Certificate Services server.</li>
<li>Specify a new path for the shared folder.</li>
</ul>


For each installation of Certificate Services, this public configuration data resides in the Certsrv.txt file, which exists in the shared folder, the Active Directory, or both. Any server set up to post its configuration information in Certsrv.txt is visible to <b>ICertConfig2</b>.

<b>ICertConfig2</b> is defined in Certcli.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertConfig2</b> interface. In Windows Server 2003 and later operating systems, the type information for this interface is also in Certclil.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertConfig2</b> interface inherits from <a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a> and <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>. <b>ICertConfig2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertConfig2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a35b2a0-f8e4-496d-b76a-a7310842cc4c">GetConfig</a>
</td>
<td align="left" width="63%">
Gets the default configuration string (the server name and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) name) for a Certificate Services server.</p> (Inherited from <a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a><b>ICertConfig2</b><b>CCertConfig</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e477fa7-d0e7-43f3-98b5-79c924a1a29c">GetField</a>
</td>
<td align="left" width="63%">
Gets a specific field from the current record of the configuration database.</p> (Inherited from <a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a><b>ICertConfig2</b><b>CCertConfig</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af81c25e-94e7-4c50-9e90-612c034e24b4">Next</a>
</td>
<td align="left" width="63%">
Points to the next available Certificate Services server configuration in the configuration point.</p> (Inherited from <a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a><b>ICertConfig2</b><b>CCertConfig</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62c24bda-463a-4238-be70-14e28bcbfb39">Reset</a>
</td>
<td align="left" width="63%">
Resets the configuration query <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a>.</p> (Inherited from <a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a><b>ICertConfig2</b><b>CCertConfig</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0fc4218-ca07-4488-bd0c-bfa8bdcd2179">SetSharedFolder</a>
</td>
<td align="left" width="63%">
Specifies a new path for the shared folder directory.</p> (Inherited from <b>ICertConfig2</b><b>CCertConfig</b>)</td>
</tr>
</table> 

