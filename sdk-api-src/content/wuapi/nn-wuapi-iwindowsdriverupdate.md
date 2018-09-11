---
UID: NN:wuapi.IWindowsDriverUpdate
title: IWindowsDriverUpdate
author: windows-sdk-content
description: Contains the properties and the methods that are available only from a Windows driver update.
old-location: wua\iwindowsdriverupdate.htm
tech.root: wua_sdk
ms.assetid: 4e2eda04-4f86-4919-b754-dba90fa8d5d8
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWindowsDriverUpdate, IWindowsDriverUpdate interface [Windows Update Agent], IWindowsDriverUpdate interface [Windows Update Agent],described, wua.iwindowsdriverupdate, wuapi/IWindowsDriverUpdate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IWindowsDriverUpdate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWindowsDriverUpdate interface


## -description


Contains the properties and the methods that are available only from a Windows driver update.


## -remarks



This interface can be obtained by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> method on an <a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a> interface only if the interface represents a Windows driver update.




## -see-also




<a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a>
 

 

