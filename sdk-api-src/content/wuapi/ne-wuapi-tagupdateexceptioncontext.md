---
UID: NE:wuapi.tagUpdateExceptionContext
title: tagUpdateExceptionContext
author: windows-sdk-content
description: Defines the context in which an IUpdateException object can be provided.
old-location: wua\updateexceptioncontext.htm
tech.root: wua_sdk
ms.assetid: ad8aa73f-10d3-40b0-8bb3-1742dac0897d
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: UpdateExceptionContext, UpdateExceptionContext enumeration [Windows Update Agent], tagUpdateExceptionContext, uecGeneral, uecWindowsDriver, uecWindowsInstaller, wua.updateexceptioncontext, wuapi/UpdateExceptionContext, wuapi/uecGeneral, wuapi/uecWindowsDriver, wuapi/uecWindowsInstaller
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - UpdateExceptionContext
product: Windows
targetos: Windows
req.typenames: UpdateExceptionContext
req.redist: 
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
 

 

