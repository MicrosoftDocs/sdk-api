---
UID: NE:wuapi.tagUpdateExceptionContext
title: UpdateExceptionContext (wuapi.h)
author: windows-sdk-content
description: Defines the context in which an IUpdateException object can be provided.
old-location: wua\updateexceptioncontext.htm
tech.root: Wua_Sdk
ms.assetid: ad8aa73f-10d3-40b0-8bb3-1742dac0897d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: UpdateExceptionContext, UpdateExceptionContext enumeration [Windows Update Agent], uecGeneral, uecWindowsDriver, uecWindowsInstaller, wua.updateexceptioncontext, wuapi/UpdateExceptionContext, wuapi/uecGeneral, wuapi/uecWindowsDriver, wuapi/uecWindowsInstaller
ms.topic: enum
f1_keywords: 
 - "wuapi/UpdateExceptionContext"
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
targetos: Windows
req.typenames: UpdateExceptionContext
req.redist: 
ms.custom: 19H1
---

# UpdateExceptionContext enumeration


## -description


Defines the context in which an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateexception">IUpdateException</a> object can be provided.


## -enum-fields




### -field uecGeneral

The <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateexception">IUpdateException</a> is not tied to any context.


### -field uecWindowsDriver

The <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateexception">IUpdateException</a> is related to one or more Windows drivers.


### -field uecWindowsInstaller

The <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateexception">IUpdateException</a> is related to Windows Installer.


### -field uecSearchIncomplete




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateexception-get_context">IUpdateException.Context</a>
 

 

