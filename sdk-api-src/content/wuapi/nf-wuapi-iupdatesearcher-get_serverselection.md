---
UID: NF:wuapi.IUpdateSearcher.get_ServerSelection
title: IUpdateSearcher::get_ServerSelection
author: windows-sdk-content
description: Gets and sets a ServerSelection value that indicates the server to search for updates.
old-location: wua\iupdatesearcherserverselection.htm
tech.root: Wua_Sdk
ms.assetid: b514545a-d983-491b-9a28-540bd5c4c128
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IUpdateSearcher interface [Windows Update Agent],ServerSelection property, IUpdateSearcher.ServerSelection, IUpdateSearcher.get_ServerSelection, IUpdateSearcher::ServerSelection, IUpdateSearcher::get_ServerSelection, IUpdateSearcher::put_ServerSelection, ServerSelection property [Windows Update Agent], ServerSelection property [Windows Update Agent],IUpdateSearcher interface, get_ServerSelection, wua.iupdatesearcherserverselection, wuapi/IUpdateSearcher::ServerSelection, wuapi/IUpdateSearcher::get_ServerSelection, wuapi/IUpdateSearcher::put_ServerSelection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wuapi.h
req.include-header: 
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
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateSearcher.ServerSelection
 - IUpdateSearcher.get_ServerSelection
 - IUpdateSearcher.put_ServerSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdateSearcher::get_ServerSelection


## -description


Gets and sets a <a href="https://msdn.microsoft.com/51caac5e-98a6-49e4-a175-6319349a6d68">ServerSelection</a> value that indicates the server to search for updates.

This property is read/write.


## -parameters


## -remarks



 The site that is not a Windows Update site that is specified by the value of the <a href="https://msdn.microsoft.com/7c00d26a-9ef0-45ec-81b3-d13f91dd7d8d">ServiceID</a> property is searched only if the value of the <b>ServerSelection</b> property is  ssOthers.




## -see-also




<a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a>
 

 

