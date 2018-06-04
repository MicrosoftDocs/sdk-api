---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagUpdateExceptionContext enumeration


## -description


Defines the context in which an <a href="https://msdn.microsoft.com/9e7458be-b411-4395-98f2-c92308f78371">IUpdateException</a> object can be provided.


## -enum-fields




### -field uecGeneral

The <a href="https://msdn.microsoft.com/9e7458be-b411-4395-98f2-c92308f78371">IUpdateException</a> is not tied to any context.


### -field uecWindowsDriver

The <a href="https://msdn.microsoft.com/9e7458be-b411-4395-98f2-c92308f78371">IUpdateException</a> is related to one or more Windows drivers.


### -field uecWindowsInstaller

The <a href="https://msdn.microsoft.com/9e7458be-b411-4395-98f2-c92308f78371">IUpdateException</a> is related to Windows Installer.


## -see-also




<a href="https://msdn.microsoft.com/05924bb7-cc59-4df6-a2dd-4e6032a0eb8b">IUpdateException.Context</a>
 

 

