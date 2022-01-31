---
UID: NE:wuapi.tagUpdateExceptionContext
title: UpdateExceptionContext (wuapi.h)
description: Defines the context in which an IUpdateException object can be provided.
helpviewer_keywords: ["UpdateExceptionContext","UpdateExceptionContext enumeration [Windows Update Agent]","uecGeneral","uecWindowsDriver","uecWindowsInstaller","wua.updateexceptioncontext","wuapi/UpdateExceptionContext","wuapi/uecGeneral","wuapi/uecWindowsDriver","wuapi/uecWindowsInstaller"]
old-location: wua\updateexceptioncontext.htm
tech.root: wua
ms.assetid: ad8aa73f-10d3-40b0-8bb3-1742dac0897d
ms.date: 12/05/2018
ms.keywords: UpdateExceptionContext, UpdateExceptionContext enumeration [Windows Update Agent], uecGeneral, uecWindowsDriver, uecWindowsInstaller, wua.updateexceptioncontext, wuapi/UpdateExceptionContext, wuapi/uecGeneral, wuapi/uecWindowsDriver, wuapi/uecWindowsInstaller
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
targetos: Windows
req.typenames: UpdateExceptionContext
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUpdateExceptionContext
 - wuapi/tagUpdateExceptionContext
 - UpdateExceptionContext
 - wuapi/UpdateExceptionContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - UpdateExceptionContext
---

# UpdateExceptionContext enumeration


## -description

Defines the context in which an <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateexception">IUpdateException</a> object can be provided.

## -enum-fields

### -field uecGeneral:1

The <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateexception">IUpdateException</a> is not tied to any context.

### -field uecWindowsDriver:2

The <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateexception">IUpdateException</a> is related to one or more Windows drivers.

### -field uecWindowsInstaller:3

The <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateexception">IUpdateException</a> is related to Windows Installer.

### -field uecSearchIncomplete:4

## -see-also

<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateexception-get_context">IUpdateException.Context</a>
