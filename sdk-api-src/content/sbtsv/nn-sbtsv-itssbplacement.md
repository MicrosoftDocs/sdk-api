---
UID: NN:sbtsv.ITsSbPlacement
title: ITsSbPlacement (sbtsv.h)
description: Exposes methods that prepare the environment (the computer that hosts the virtual machine).
helpviewer_keywords: ["ITsSbPlacement","ITsSbPlacement interface [Remote Desktop Services]","ITsSbPlacement interface [Remote Desktop Services]","described","sbtsv/ITsSbPlacement","termserv.itssbplacement"]
old-location: termserv\itssbplacement.htm
tech.root: TermServ
ms.assetid: d90501dd-ca15-463c-b204-b1f56103ebe7
ms.date: 12/05/2018
ms.keywords: ITsSbPlacement, ITsSbPlacement interface [Remote Desktop Services], ITsSbPlacement interface [Remote Desktop Services],described, sbtsv/ITsSbPlacement, termserv.itssbplacement
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
 - ITsSbPlacement
 - sbtsv/ITsSbPlacement
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
 - ITsSbPlacement
---

# ITsSbPlacement interface


## -description

Exposes methods that prepare the environment (the computer that hosts the virtual 
machine). After Remote Desktop Connection Broker (RD Connection Broker) receives a load-balancing result, it calls <a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbplacement-queryenvironmentfortarget">QueryEnvironmentForTarget</a> 
to determine whether the environment is present and ready.

## -inheritance

The <b>ITsSbPlacement</b> interface inherits from <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>. <b>ITsSbPlacement</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
