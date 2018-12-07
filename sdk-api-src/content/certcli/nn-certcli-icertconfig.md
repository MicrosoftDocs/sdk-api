---
UID: NN:certcli.ICertConfig
title: ICertConfig
author: windows-sdk-content
description: The ICertConfig interface provides functionality for retrieving the public configuration data (specified during client setup) for a Certificate Services server.
old-location: security\icertconfig.htm
tech.root: seccrypto
ms.assetid: 92bece6a-73f0-47cf-8142-77e986448824
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICertConfig, ICertConfig interface [Security], ICertConfig interface [Security],described, _certsrv_icertconfig, certcli/ICertConfig, security.icertconfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: certcli.h
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
req.dll: Certcli.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertConfig interface


## -description


The <b>ICertConfig</b> interface provides functionality for retrieving  the public  configuration data (specified during client setup) for a Certificate Services server.
			


The <b>ICertConfig</b> interface is used to perform the following tasks:

<ul>
<li>Enumerate through the  configuration strings for a Certificate Services server in the configuration point.</li>
<li>Retrieve the  default  configuration for a Certificate Services server.</li>
<li>Retrieve the  details of a specific Certificate Services server configuration.</li>
<li>Reset the configuration of a Certificate Services server.</li>
</ul>


For each installation of Certificate Services, this public configuration data resides in the Certsrv.txt file, which exists in the shared folder, the Active Directory, or both. Any server set up to post its configuration information in Certsrv.txt is visible to <b>ICertConfig</b>.

<b>ICertConfig</b> is defined in Certcli.h. When you create your program, however, use Certsrv.h as the include file. Certcli.dll provides the <b>ICertConfig</b> interface. The type information for this interface is also in Certclil.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertConfig</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ICertConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383274(v=VS.85).aspx">GetConfig</a>
</td>
<td align="left" width="63%">
Gets the default configuration string (the server name and <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) name) for a Certificate Services server.</p> (Inherited from <b>ICertConfig</b><a href="https://msdn.microsoft.com/en-us/library/Aa383272(v=VS.85).aspx">ICertConfig2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa383272(v=VS.85).aspx">CCertConfig</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383277(v=VS.85).aspx">GetField</a>
</td>
<td align="left" width="63%">
Gets a specific field from the current record of the configuration database.</p> (Inherited from <b>ICertConfig</b><a href="https://msdn.microsoft.com/en-us/library/Aa383272(v=VS.85).aspx">ICertConfig2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa383272(v=VS.85).aspx">CCertConfig</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383280(v=VS.85).aspx">Next</a>
</td>
<td align="left" width="63%">
Points to the next available Certificate Services server configuration in the configuration point.</p> (Inherited from <b>ICertConfig</b><a href="https://msdn.microsoft.com/en-us/library/Aa383272(v=VS.85).aspx">ICertConfig2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa383272(v=VS.85).aspx">CCertConfig</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa383282(v=VS.85).aspx">Reset</a>
</td>
<td align="left" width="63%">
Resets the configuration query <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">state</a>.</p> (Inherited from <b>ICertConfig</b><a href="https://msdn.microsoft.com/en-us/library/Aa383272(v=VS.85).aspx">ICertConfig2</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa383272(v=VS.85).aspx">CCertConfig</a>)</td>
</tr>
</table> 

