---
UID: NF:shobjidl_core.ISearchFolderItemFactory.SetFolderLogicalViewMode
title: ISearchFolderItemFactory::SetFolderLogicalViewMode
author: windows-sdk-content
description: Sets folder logical view mode. The default settings are based on the FolderTypeID which is set by the ISearchFolderItemFactory::SetFolderTypeID method.
old-location: shell\ISearchFolderItemFactory_SetFolderLogicalViewMode.htm
old-project: shell
ms.assetid: ef72f196-cfd5-4547-85cb-0ccfdc496c46
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ISearchFolderItemFactory interface [Windows Shell],SetFolderLogicalViewMode method, ISearchFolderItemFactory.SetFolderLogicalViewMode, ISearchFolderItemFactory::SetFolderLogicalViewMode, SetFolderLogicalViewMode, SetFolderLogicalViewMode method [Windows Shell], SetFolderLogicalViewMode method [Windows Shell],ISearchFolderItemFactory interface, _shell_ISearchFolderItemFactory_SetFolderLogicalViewMode, shell.ISearchFolderItemFactory_SetFolderLogicalViewMode, shobjidl_core/ISearchFolderItemFactory::SetFolderLogicalViewMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ISearchFolderItemFactory.SetFolderLogicalViewMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISearchFolderItemFactory::SetFolderLogicalViewMode


## -description



      Sets folder logical view mode. The default settings are based on the <code>FolderTypeID</code> which is set by the <a href="https://msdn.microsoft.com/a9b09dc6-751e-4d5f-b016-0b26c15c68f6">ISearchFolderItemFactory::SetFolderTypeID</a> method.


## -parameters




### -param flvm [in]

Type: <b><a href="https://msdn.microsoft.com/4b30a335-ed80-4774-82d4-bc93c95ee80c">FOLDERLOGICALVIEWMODE</a></b>


          The <a href="https://msdn.microsoft.com/4b30a335-ed80-4774-82d4-bc93c95ee80c">FOLDERLOGICALVIEWMODE</a> value.
        


## -returns



Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.



