---
UID: NF:certadm.IOCSPAdmin.Ping
title: IOCSPAdmin::Ping (certadm.h)
description: Tests a DCOM connection with an Online Certificate Status Protocol (OCSP) responder service.
helpviewer_keywords: ["IOCSPAdmin interface [Security]","Ping method","IOCSPAdmin.Ping","IOCSPAdmin::Ping","Ping","Ping method [Security]","Ping method [Security]","IOCSPAdmin interface","certadm/IOCSPAdmin::Ping","security.iocspadmin_ping"]
old-location: security\iocspadmin_ping.htm
tech.root: security
ms.assetid: 55d224c7-f309-471a-b2e5-38b8e2b8e00c
ms.date: 12/05/2018
ms.keywords: IOCSPAdmin interface [Security],Ping method, IOCSPAdmin.Ping, IOCSPAdmin::Ping, Ping, Ping method [Security], Ping method [Security],IOCSPAdmin interface, certadm/IOCSPAdmin::Ping, security.iocspadmin_ping
req.header: certadm.h
req.include-header: Certsrv.h
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
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCSPAdmin::Ping
 - certadm/IOCSPAdmin::Ping
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPAdmin.Ping
---

# IOCSPAdmin::Ping


## -description

The <b>Ping</b> method tests a DCOM connection with an Online Certificate Status Protocol (OCSP) responder service.

## -parameters

### -param bstrServerName [in]

A string that contains the OCSP responder server name.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a>