---
UID: NE:wbemdisp.WbemConnectOptionsEnum
title: WbemConnectOptionsEnum
author: windows-sdk-content
description: Defines a security flag that is used as a parameter in calls to the SWbemLocator.ConnectServer method when a connection to WMI on a remote machine is failing.
old-location: wmi\wbemconnectoptionsenum.htm
tech.root: WmiSdk
ms.assetid: 781121e9-9dea-408c-a241-0c9f28c2cd46
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: WbemConnectOptionsEnum, WbemConnectOptionsEnum enumeration [Windows Management Instrumentation], _hmm_wbemconnectoptionsenum, wbemConnectFlagUseMaxWait, wbemdisp/WbemConnectOptionsEnum, wbemdisp/wbemConnectFlagUseMaxWait, wmi.wbemconnectoptionsenum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
---

# WbemConnectOptionsEnum enumeration


## -description


The 
WbemConnectOptionsEnum constant defines a security flag that is used as a parameter in calls to 
the <a href="https://msdn.microsoft.com/31364c68-b031-4cf0-851f-b4e302f077e0">SWbemLocator.ConnectServer</a> method when a connection to WMI on a remote machine is failing.


## -enum-fields




### -field wbemConnectFlagUseMaxWait

Shortens the timeout for the <a href="https://msdn.microsoft.com/31364c68-b031-4cf0-851f-b4e302f077e0">SWbemLocator.ConnectServer</a> method call to two minutes.


## -see-also




<a href="https://msdn.microsoft.com/feaab757-3167-420b-8f42-edced4cd4c53">Scripting API Constants</a>
 

 

