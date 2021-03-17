---
UID: NF:sbtsv.ITsSbEnvironment.get_ServerWeight
title: ITsSbEnvironment::get_ServerWeight (sbtsv.h)
description: Retrieves a value that indicates the server weight of the environment that hosts the target computer.
helpviewer_keywords: ["ITsSbEnvironment interface [Remote Desktop Services]","ServerWeight property","ITsSbEnvironment.ServerWeight","ITsSbEnvironment.get_ServerWeight","ITsSbEnvironment::ServerWeight","ITsSbEnvironment::get_ServerWeight","ServerWeight property [Remote Desktop Services]","ServerWeight property [Remote Desktop Services]","ITsSbEnvironment interface","get_ServerWeight","sbtsv/ITsSbEnvironment::ServerWeight","sbtsv/ITsSbEnvironment::get_ServerWeight","termserv.itssbenvironment_serverweight"]
old-location: termserv\itssbenvironment_serverweight.htm
tech.root: TermServ
ms.assetid: 1c8119ec-22ce-4405-8b30-8cb0c3e2f1c6
ms.date: 12/05/2018
ms.keywords: ITsSbEnvironment interface [Remote Desktop Services],ServerWeight property, ITsSbEnvironment.ServerWeight, ITsSbEnvironment.get_ServerWeight, ITsSbEnvironment::ServerWeight, ITsSbEnvironment::get_ServerWeight, ServerWeight property [Remote Desktop Services], ServerWeight property [Remote Desktop Services],ITsSbEnvironment interface, get_ServerWeight, sbtsv/ITsSbEnvironment::ServerWeight, sbtsv/ITsSbEnvironment::get_ServerWeight, termserv.itssbenvironment_serverweight
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - ITsSbEnvironment::get_ServerWeight
 - sbtsv/ITsSbEnvironment::get_ServerWeight
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbEnvironment.ServerWeight
 - ITsSbEnvironment.get_ServerWeight
---

# ITsSbEnvironment::get_ServerWeight


## -description

Retrieves a value that indicates the server weight of the environment that hosts the target computer.

This property is read-only.

## -parameters

## -remarks

Plug-ins can use the server weight to make load balancing decisions. This value is not used by Remote Desktop Connection Broker (RD Connection Broker).

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a>