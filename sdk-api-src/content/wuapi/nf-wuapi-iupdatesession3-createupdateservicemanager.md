---
UID: NF:wuapi.IUpdateSession3.CreateUpdateServiceManager
title: IUpdateSession3::CreateUpdateServiceManager
author: windows-sdk-content
description: Returns a pointer to an IUpdateServiceManager2 interface for the session.
old-location: wua\iupdatesession3_createupdateservicemanager.htm
old-project: Wua_Sdk
ms.assetid: 79d8f489-5375-48e2-a40d-d6f38f4843aa
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CreateUpdateServiceManager, CreateUpdateServiceManager method [Windows Update Agent], CreateUpdateServiceManager method [Windows Update Agent],IUpdateSession3 interface, IUpdateSession3 interface [Windows Update Agent],CreateUpdateServiceManager method, IUpdateSession3.CreateUpdateServiceManager, IUpdateSession3::CreateUpdateServiceManager, wua.iupdatesession3_createupdateservicemanager, wuapi/IUpdateSession3::CreateUpdateServiceManager
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateSession3.CreateUpdateServiceManager
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateSession3::CreateUpdateServiceManager


## -description


Returns a pointer to an <a href="https://msdn.microsoft.com/26b75edc-eb43-4ee0-8040-da8b3252cf21">IUpdateServiceManager2</a> interface for the session.


## -parameters




### -param retval [out]

A pointer to an <a href="https://msdn.microsoft.com/26b75edc-eb43-4ee0-8040-da8b3252cf21">IUpdateServiceManager2</a> interface for the session.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/7caa07ee-ec78-45eb-99a2-0e6682790c88">IUpdateSession3</a>
 

 

