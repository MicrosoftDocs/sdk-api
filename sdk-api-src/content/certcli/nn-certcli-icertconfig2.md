---
UID: NN:certcli.ICertConfig2
title: ICertConfig2 (certcli.h)
description: Provide functionality for retrieving the public configuration data (specified during client setup) for a Certificate Services server.
helpviewer_keywords: ["ICertConfig2","ICertConfig2 interface [Security]","ICertConfig2 interface [Security]","described","_certsrv_icertconfig2","certcli/ICertConfig2","security.icertconfig2"]
old-location: security\icertconfig2.htm
tech.root: security
ms.assetid: 6bac5961-f9cc-4859-affa-aa7ed152ebfa
ms.date: 12/05/2018
ms.keywords: ICertConfig2, ICertConfig2 interface [Security], ICertConfig2 interface [Security],described, _certsrv_icertconfig2, certcli/ICertConfig2, security.icertconfig2
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
 - ICertConfig2
 - certcli/ICertConfig2
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
 - ICertConfig2
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

The <b>ICertConfig2</b> interface inherits from <a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a> and <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>. <b>ICertConfig2</b> also has these types of members:

