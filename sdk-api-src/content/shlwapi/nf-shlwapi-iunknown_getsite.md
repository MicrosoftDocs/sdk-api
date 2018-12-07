---
UID: NF:shlwapi.IUnknown_GetSite
title: IUnknown_GetSite function
author: windows-sdk-content
description: Calls the specified object's IObjectWithSite::GetSite method.
old-location: shell\IUnknown_GetSite.htm
tech.root: shell
ms.assetid: 95e83078-ab74-40d6-8e31-653e578770f2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUnknown_GetSite, IUnknown_GetSite function [Windows Shell], _win32_IUnknown_GetSite, shell.IUnknown_GetSite, shlwapi/IUnknown_GetSite
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-comhelpers-l1-1-0.dll
api_name:
 - IUnknown_GetSite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUnknown_GetSite function


## -description


Calls the specified object's <a href="https://msdn.microsoft.com/f88ef2b1-63c3-4307-a5e1-b9104c8aef29">IObjectWithSite::GetSite</a> method.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the COM object whose <a href="https://msdn.microsoft.com/f88ef2b1-63c3-4307-a5e1-b9104c8aef29">IObjectWithSite::GetSite</a> method is to be called.


### -param riid [in]

Type: <b>REFIID</b>

The IID of the interface pointer that should be returned in <i>ppvSite</i>.


### -param ppv [out]

Type: <b>VOID**</b>

The address of the pointer to receive the requested interface pointer. If the function call is successful, <i>ppvSite</i> will contain the requested interface pointer. If no site is available or the requested interface is not supported, <i>ppvSite</i> is set to <b>NULL</b> and the function returns a COM error code.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the site was successfully retrieved or a COM error code otherwise.




## -remarks



This function calls the specified object's <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method to obtain the <a href="https://msdn.microsoft.com/e688136e-e06b-46ba-bec9-b8db2f9c468d">IObjectWithSite</a> interface.  If successful, the function calls the interface's <a href="https://msdn.microsoft.com/f88ef2b1-63c3-4307-a5e1-b9104c8aef29">IObjectWithSite::GetSite</a> method to obtain the site.



