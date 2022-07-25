---
UID: NN:certcli.ICertConfig
title: ICertConfig (certcli.h)
description: The ICertConfig interface provides functionality for retrieving the public configuration data (specified during client setup) for a Certificate Services server.
helpviewer_keywords: ["ICertConfig","ICertConfig interface [Security]","ICertConfig interface [Security]","described","_certsrv_icertconfig","certcli/ICertConfig","security.icertconfig"]
old-location: security\icertconfig.htm
tech.root: security
ms.assetid: 92bece6a-73f0-47cf-8142-77e986448824
ms.date: 12/05/2018
ms.keywords: ICertConfig, ICertConfig interface [Security], ICertConfig interface [Security],described, _certsrv_icertconfig, certcli/ICertConfig, security.icertconfig
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertConfig
 - certcli/ICertConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertConfig
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

The <b>ICertConfig</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertConfig</b> also has these types of members:

