---
UID: NF:wuapi.IUpdateService.get_Name
title: IUpdateService::get_Name
author: windows-sdk-content
description: Gets the name of the service.
old-location: wua\iupdateservice_name.htm
old-project: Wua_Sdk
ms.assetid: 37c84d46-628f-4af9-ac40-8ba2c5a24fd6
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IUpdateService interface [Windows Update Agent],Name property, IUpdateService.Name, IUpdateService.get_Name, IUpdateService::Name, IUpdateService::get_Name, Name property [Windows Update Agent], Name property [Windows Update Agent],IUpdateService interface, get_Name, wua.iupdateservice_name, wuapi/IUpdateService::Name, wuapi/IUpdateService::get_Name
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IUpdateService.Name
-	IUpdateService.get_Name
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateService::get_Name


## -description


Gets the name of the service.

This property is read-only.


## -parameters


## -remarks



The localized properties of an update are returned in the language that corresponds to the user default user interface (UI) language of the caller. If a property of an update is unavailable in such language, it will be returned in the system default UI language on the specified computer. If the property is unavailable in either languages mentioned, then it will be returned in the language recommended, if any, by the provider of the Update. Otherwise the Update Service will choose a language as it sees fit for the property.




## -see-also




<a href="https://msdn.microsoft.com/2f237cd3-668b-4b1b-b98b-4cfc40f5889e">IUpdateService</a>
 

 

