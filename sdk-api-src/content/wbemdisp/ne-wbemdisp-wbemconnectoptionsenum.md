---
UID: NE:wbemdisp.WbemConnectOptionsEnum
title: WbemConnectOptionsEnum (wbemdisp.h)
description: Defines a security flag that is used as a parameter in calls to the SWbemLocator.ConnectServer method when a connection to WMI on a remote machine is failing.
helpviewer_keywords: ["WbemConnectOptionsEnum","WbemConnectOptionsEnum enumeration [Windows Management Instrumentation]","_hmm_wbemconnectoptionsenum","wbemConnectFlagUseMaxWait","wbemdisp/WbemConnectOptionsEnum","wbemdisp/wbemConnectFlagUseMaxWait","wmi.wbemconnectoptionsenum"]
old-location: wmi\wbemconnectoptionsenum.htm
tech.root: wmi
ms.assetid: 781121e9-9dea-408c-a241-0c9f28c2cd46
ms.date: 12/05/2018
ms.keywords: WbemConnectOptionsEnum, WbemConnectOptionsEnum enumeration [Windows Management Instrumentation], _hmm_wbemconnectoptionsenum, wbemConnectFlagUseMaxWait, wbemdisp/WbemConnectOptionsEnum, wbemdisp/wbemConnectFlagUseMaxWait, wmi.wbemconnectoptionsenum
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wbemdisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WbemConnectOptionsEnum
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WbemConnectOptionsEnum
 - wbemdisp/WbemConnectOptionsEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemdisp.h
api_name:
 - WbemConnectOptionsEnum
---

# WbemConnectOptionsEnum enumeration


## -description

The 
WbemConnectOptionsEnum constant defines a security flag that is used as a parameter in calls to 
the <a href="/windows/desktop/WmiSdk/swbemlocator-connectserver">SWbemLocator.ConnectServer</a> method when a connection to WMI on a remote machine is failing.

## -enum-fields

### -field wbemConnectFlagUseMaxWait:0x80

Shortens the timeout for the <a href="/windows/desktop/WmiSdk/swbemlocator-connectserver">SWbemLocator.ConnectServer</a> method call to two minutes.

## -see-also

<a href="/windows/desktop/WmiSdk/scripting-api-constants">Scripting API Constants</a>
