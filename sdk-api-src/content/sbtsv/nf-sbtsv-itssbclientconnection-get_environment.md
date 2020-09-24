---
UID: NF:sbtsv.ITsSbClientConnection.get_Environment
title: ITsSbClientConnection::get_Environment (sbtsv.h)
description: Retrieves an object that contains information about the environment that hosts the target computer.
helpviewer_keywords: ["Environment property [Remote Desktop Services]","Environment property [Remote Desktop Services]","ITsSbClientConnection interface","ITsSbClientConnection interface [Remote Desktop Services]","Environment property","ITsSbClientConnection.Environment","ITsSbClientConnection.get_Environment","ITsSbClientConnection::Environment","ITsSbClientConnection::get_Environment","get_Environment","sbtsv/ITsSbClientConnection::Environment","sbtsv/ITsSbClientConnection::get_Environment","termserv.itssbclientconnection_environment"]
old-location: termserv\itssbclientconnection_environment.htm
tech.root: TermServ
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.date: 12/05/2018
ms.keywords: Environment property [Remote Desktop Services], Environment property [Remote Desktop Services],ITsSbClientConnection interface, ITsSbClientConnection interface [Remote Desktop Services],Environment property, ITsSbClientConnection.Environment, ITsSbClientConnection.get_Environment, ITsSbClientConnection::Environment, ITsSbClientConnection::get_Environment, get_Environment, sbtsv/ITsSbClientConnection::Environment, sbtsv/ITsSbClientConnection::get_Environment, termserv.itssbclientconnection_environment
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
 - ITsSbClientConnection::get_Environment
 - sbtsv/ITsSbClientConnection::get_Environment
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
 - ITsSbClientConnection.Environment
 - ITsSbClientConnection.get_Environment
---

# ITsSbClientConnection::get_Environment


## -description

Retrieves an object that contains information about the environment that hosts the target computer. For example, in a virtual desktop scenario, this object would contain information about the computer that hosts the virtual machine.

This property is read-only.

## -parameters

## -remarks

An orchestration plug-in can call this method to retrieve environment information about a target virtual machine.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a>