---
UID: NE:wbemdisp.WbemConnectOptionsEnum
title: WbemConnectOptionsEnum (wbemdisp.h)
author: windows-sdk-content
description: Defines a security flag that is used as a parameter in calls to the SWbemLocator.ConnectServer method when a connection to WMI on a remote machine is failing.
old-location: wmi\wbemconnectoptionsenum.htm
tech.root: WmiSdk
ms.assetid: 781121e9-9dea-408c-a241-0c9f28c2cd46
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WbemConnectOptionsEnum, WbemConnectOptionsEnum enumeration [Windows Management Instrumentation], _hmm_wbemconnectoptionsenum, wbemConnectFlagUseMaxWait, wbemdisp/WbemConnectOptionsEnum, wbemdisp/wbemConnectFlagUseMaxWait, wmi.wbemconnectoptionsenum
ms.topic: enum
f1_keywords: ["wbemdisp/WbemConnectOptionsEnum"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemdisp.h
api_name:
 - WbemConnectOptionsEnum
product: Windows
targetos: Windows
req.typenames: WbemConnectOptionsEnum
req.redist: 
ms.custom: 19H1
---

# WbemConnectOptionsEnum enumeration


## -description


The 
WbemConnectOptionsEnum constant defines a security flag that is used as a parameter in calls to 
the <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/swbemlocator-connectserver">SWbemLocator.ConnectServer</a> method when a connection to WMI on a remote machine is failing.


## -enum-fields




### -field wbemConnectFlagUseMaxWait

Shortens the timeout for the <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/swbemlocator-connectserver">SWbemLocator.ConnectServer</a> method call to two minutes.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/scripting-api-constants">Scripting API Constants</a>
 

 

