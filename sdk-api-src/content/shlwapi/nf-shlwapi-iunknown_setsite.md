---
UID: NF:shlwapi.IUnknown_SetSite
title: IUnknown_SetSite function
author: windows-sdk-content
description: Sets the specified object's site by calling its IObjectWithSite::SetSite method.
old-location: shell\IUnknown_SetSite.htm
old-project: shell
ms.assetid: 66175435-f85b-4e26-b148-f4edb74cb41d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUnknown_SetSite, IUnknown_SetSite function [Windows Shell], _win32_IUnknown_SetSite, shell.IUnknown_SetSite, shlwapi/IUnknown_SetSite
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
-	ShCore.dll
-	API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
-	API-MS-Win-ShCore-comhelpers-l1-1-0.dll
api_name:
-	IUnknown_SetSite
product: Windows
targetos: Windows
req.lib: 
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# IUnknown_SetSite function


## -description


Sets the specified object's site by calling its <a href="https://msdn.microsoft.com/5e95b2a6-85b3-4899-9e23-54ed9e69e821">IObjectWithSite::SetSite</a> method.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the IUnknown interface of the object whose site is to be changed.


### -param punkSite [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the IUnknown interface of the new site.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the site was successfully set, or a COM error code otherwise.




## -remarks



This function calls the specified object's IUnknown::QueryInterface method to obtain a pointer to the object's <a href="https://msdn.microsoft.com/e688136e-e06b-46ba-bec9-b8db2f9c468d">IObjectWithSite</a> interface.  If successful, the function calls <a href="https://msdn.microsoft.com/5e95b2a6-85b3-4899-9e23-54ed9e69e821">IObjectWithSite::SetSite</a> to set or change the site.



