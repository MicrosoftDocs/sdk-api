---
UID: NE:wuapicommon.tagServerSelection
title: ServerSelection (wuapicommon.h)
description: Defines the update services that Windows Update can operate against.
helpviewer_keywords: ["ServerSelection","ServerSelection enumeration [Windows Update Agent]","ssDefault","ssManagedServer","ssOthers","ssWindowsUpdate","wua.serverselection","wuapicommon/ServerSelection","wuapicommon/ssDefault","wuapicommon/ssManagedServer","wuapicommon/ssOthers","wuapicommon/ssWindowsUpdate"]
old-location: wua\serverselection.htm
tech.root: wua
ms.assetid: 51caac5e-98a6-49e4-a175-6319349a6d68
ms.date: 12/05/2018
ms.keywords: ServerSelection, ServerSelection enumeration [Windows Update Agent], ssDefault, ssManagedServer, ssOthers, ssWindowsUpdate, wua.serverselection, wuapicommon/ServerSelection, wuapicommon/ssDefault, wuapicommon/ssManagedServer, wuapicommon/ssOthers, wuapicommon/ssWindowsUpdate
f1_keywords:
- wuapicommon/ServerSelection
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- wuapicommon.h
api_name:
- ServerSelection
targetos: Windows
req.typenames: ServerSelection
req.redist: 
ms.custom: 19H1
---

# ServerSelection enumeration


## -description


Defines the update services that Windows Update can operate against. 


## -enum-fields




### -field ssDefault

Used only by <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a>. Indicates that the search call should search the default server.

The default server used by the Windows Update Agent (WUA) is the same as <b>ssMangagedServer</b> if the computer is set up to have a managed server. If the computer is not been set up to have a managed server, WUA uses the first update service for which the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateservice-get_isregisteredwithau">IsRegisteredWithAU</a> property of <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservice">IUpdateService</a> is VARIANT_TRUE and the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateservice-get_ismanaged">IsManaged</a> property of <b>IUpdateService</b> is VARIANT_FALSE


### -field ssManagedServer

Indicates the managed server, in an environment that uses Windows Server Update Services or a similar corporate update server to manage the computer.


### -field ssWindowsUpdate

Indicates the Windows Update service.


### -field ssOthers

Indicates some update service other than those listed previously. If the <b>ServerSelection</b> property of a Windows Update Agent API object is set to <b>ssOthers</b>, then the <b>ServiceID</b> property of the object contains the ID of the service.