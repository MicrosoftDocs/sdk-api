---
UID: NF:sbtsv.ITsSbTarget.get_TargetLoad
title: ITsSbTarget::get_TargetLoad (sbtsv.h)
description: Retrieves the relative load on a target.
helpviewer_keywords: ["ITsSbTarget interface [Remote Desktop Services]","TargetLoad property","ITsSbTarget.TargetLoad","ITsSbTarget.get_TargetLoad","ITsSbTarget::TargetLoad","ITsSbTarget::get_TargetLoad","ITsSbTargetEx interface [Remote Desktop Services]","TargetLoad property","ITsSbTargetEx.TargetLoad","ITsSbTargetEx::get_TargetLoad","TargetLoad property [Remote Desktop Services]","TargetLoad property [Remote Desktop Services]","ITsSbTarget interface","TargetLoad property [Remote Desktop Services]","ITsSbTargetEx interface","get_TargetLoad","sbtsv/ITsSbTarget::TargetLoad","sbtsv/ITsSbTarget::get_TargetLoad","sbtsv/ITsSbTargetEx::TargetLoad","sbtsv/ITsSbTargetEx::get_TargetLoad","termserv.itssbtarget_targetload"]
old-location: termserv\itssbtarget_targetload.htm
tech.root: TermServ
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.date: 12/05/2018
ms.keywords: ITsSbTarget interface [Remote Desktop Services],TargetLoad property, ITsSbTarget.TargetLoad, ITsSbTarget.get_TargetLoad, ITsSbTarget::TargetLoad, ITsSbTarget::get_TargetLoad, ITsSbTargetEx interface [Remote Desktop Services],TargetLoad property, ITsSbTargetEx.TargetLoad, ITsSbTargetEx::get_TargetLoad, TargetLoad property [Remote Desktop Services], TargetLoad property [Remote Desktop Services],ITsSbTarget interface, TargetLoad property [Remote Desktop Services],ITsSbTargetEx interface, get_TargetLoad, sbtsv/ITsSbTarget::TargetLoad, sbtsv/ITsSbTarget::get_TargetLoad, sbtsv/ITsSbTargetEx::TargetLoad, sbtsv/ITsSbTargetEx::get_TargetLoad, termserv.itssbtarget_targetload
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - ITsSbTarget::get_TargetLoad
 - sbtsv/ITsSbTarget::get_TargetLoad
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
 - ITsSbTarget.TargetLoad
 - ITsSbTarget.get_TargetLoad
 - ITsSbTargetEx.TargetLoad
 - ITsSbTargetEx.get_TargetLoad
---

# ITsSbTarget::get_TargetLoad


## -description

Retrieves the relative load on a target. This value is based on the number of existing and pending sessions. By default a pending session has the same value as an existing session.

This property is read-only.

## -parameters

## -remarks

The weight of a pending session relative to an active session can be changed by setting the value of the <i>LB_ConnectionEstablishmentPenalty</i> parameter for the Connection Broker. This parameter is located under the <b>HKLM\System\CurrentControlSet\Services\Tssdis\Parameters</b> registry key. The default value of 1 specifies that pending sessions have the same weight as active sessions.

This property is available on Windows Server 2012 R2 with <a href="https://support.microsoft.com/help/3091411/user-connection-fails-when-many-connections-are-made-to-windows-server">KB3091411</a> installed in the <a href="/windows/desktop/TermServ/itssbtargetex">ITsSbTargetEx</a> interface.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a>



<a href="/windows/desktop/TermServ/itssbtargetex">ITsSbTargetEx</a>