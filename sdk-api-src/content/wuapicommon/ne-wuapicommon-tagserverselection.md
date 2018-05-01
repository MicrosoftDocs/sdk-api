---
UID: NE:wuapicommon.tagServerSelection
title: tagServerSelection
author: windows-driver-content
description: Defines the update services that Windows Update can operate against.
old-location: wua\serverselection.htm
old-project: Wua_Sdk
ms.assetid: 51caac5e-98a6-49e4-a175-6319349a6d68
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: ServerSelection, ServerSelection enumeration [Windows Update Agent], ssDefault, ssManagedServer, ssOthers, ssWindowsUpdate, tagServerSelection, wua.serverselection, wuapicommon/ServerSelection, wuapicommon/ssDefault, wuapicommon/ssManagedServer, wuapicommon/ssOthers, wuapicommon/ssWindowsUpdate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wuapicommon.h
req.include-header: Wuapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ServerSelection
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wuapicommon.h
api_name:
-	ServerSelection
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# tagServerSelection enumeration


## -description


Defines the update services that Windows Update can operate against. 


## -enum-fields




### -field ssDefault

Used only by <a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a>. Indicates that the search call should search the default server.

The default server used by the Windows Update Agent (WUA) is the same as <b>ssMangagedServer</b> if the computer is set up to have a managed server. If the computer is not been set up to have a managed server, WUA uses the first update service for which the <a href="https://msdn.microsoft.com/17b51a04-69f6-4a96-880b-ef57f75253ae">IsRegisteredWithAU</a> property of <a href="https://msdn.microsoft.com/2f237cd3-668b-4b1b-b98b-4cfc40f5889e">IUpdateService</a> is VARIANT_TRUE and the <a href="https://msdn.microsoft.com/1a473cb3-7209-4056-91bc-bfa416981ae5">IsManaged</a> property of <b>IUpdateService</b> is VARIANT_FALSE


### -field ssManagedServer

Indicates the managed server, in an environment that uses Windows Server Update Services or a similar corporate update server to manage the computer.


### -field ssWindowsUpdate

Indicates the Windows Update service.


### -field ssOthers

Indicates some update service other than those listed previously. If the <b>ServerSelection</b> property of a Windows Update Agent API object is set to <b>ssOthers</b>, then the <b>ServiceID</b> property of the object contains the ID of the service.

