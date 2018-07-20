---
UID: NN:certadm.IOCSPCAConfiguration
title: IOCSPCAConfiguration
author: windows-sdk-content
description: Represents a set of definitions that enable an Online Certificate Status Protocol (OCSP) service to respond to a certificate status request for a specific certification authority (CA).
old-location: security\iocspcaconfiguration.htm
old-project: seccrypto
ms.assetid: 57900e1e-9c51-4c1b-aa42-634b6c3a9999
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IOCSPCAConfiguration, IOCSPCAConfiguration interface [Security], IOCSPCAConfiguration interface [Security],described, certadm/IOCSPCAConfiguration, security.iocspcaconfiguration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certadm.h
req.include-header: Certserv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certadm.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPCAConfiguration
product: Windows
targetos: Windows
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
---

# IOCSPCAConfiguration interface


## -description


The <b>IOCSPCAConfiguration</b> interface represents a set of definitions that enable an Online Certificate Status Protocol (OCSP) service to respond to a certificate status request for a specific <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA).

Microsoft provides a default implementation of this interface in the <b>OCSPCAConfiguration</b> class. An <b>OCSPCAConfiguration</b> object cannot be created externally. An <b>OCSPCAConfiguration</b> object can only be created by using the <a href="https://msdn.microsoft.com/d1c47402-77b1-4c43-8d57-20b9dd2682f7">CreateCAConfiguration</a> method.

 The default implementations of <a href="https://msdn.microsoft.com/cf76e934-07a2-46de-b2cf-7f6d3e274d71">IOCSPAdmin</a> and <a href="https://msdn.microsoft.com/4e232c34-b5ab-4269-903b-189aac5a8ddc">IOCSPCAConfigurationCollection</a> methods create a <b>OCSPCAConfiguration</b> object and use its properties.


## -see-also




<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

