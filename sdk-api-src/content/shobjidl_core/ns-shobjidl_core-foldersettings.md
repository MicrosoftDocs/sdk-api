---
UID: NS:shobjidl_core.FOLDERSETTINGS
title: FOLDERSETTINGS
author: windows-sdk-content
description: Contains folder view information.
old-location: shell\FOLDERSETTINGS.htm
old-project: shell
ms.assetid: be00fe39-1add-412e-b88b-4b0b1404b19d
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: "*LPFOLDERSETTINGS, *PFOLDERSETTINGS, FOLDERSETTINGS, FOLDERSETTINGS structure [Windows Shell], _win32_FOLDERSETTINGS, shell.FOLDERSETTINGS, shobjidl_core/FOLDERSETTINGS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FOLDERSETTINGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - FOLDERSETTINGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# FOLDERSETTINGS structure


## -description


Contains folder view information.


## -struct-fields




### -field ViewMode

Type: <b>UINT</b>

Folder view mode. One of the <a href="https://msdn.microsoft.com/16b92115-6e7d-41d3-960d-6783d779224c">FOLDERVIEWMODE</a> values.


### -field fFlags

Type: <b>UINT</b>

A set of flags that indicate the options for the folder. This can be zero or a combination of the <a href="https://msdn.microsoft.com/e471b81a-da4d-48c0-8c7f-996b507d27a1">FOLDERFLAGS</a> values.


## -remarks



These settings assume a particular user interface, which the Shell's folder view has. A Shell extension can use these settings if they apply to the view implemented by the extension.




## -see-also




<a href="https://msdn.microsoft.com/62d71bca-d2cb-4668-b0bf-2e53756f2cd9">IShellView::CreateViewWindow</a>



<a href="https://msdn.microsoft.com/69d18b4f-3a68-420c-a184-05c2f69a5ec6">IShellView::GetCurrentInfo</a>
 

 

