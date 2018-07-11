---
UID: NF:shldisp.FolderItems3.Filter
title: FolderItems3::Filter
author: windows-sdk-content
description: Sets a wildcard filter to apply to the items returned.
old-location: shell\FolderItems3_Filter.htm
old-project: shell
ms.assetid: 19ca82c5-16ff-46c7-8ea1-ddbfc2ce3ac9
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: Filter, Filter method [Windows Shell], Filter method [Windows Shell],FolderItems3 object, FolderItems3 object [Windows Shell],Filter method, FolderItems3.Filter, FolderItems3::Filter, _win32_FolderItems3_Filter, shell.FolderItems3_Filter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - FolderItems3.Filter
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# FolderItems3::Filter


## -description


Sets a wildcard filter to apply to the items returned.


## -parameters




### -param grfFlags [in]

Type: <b>Integer</b>

This parameter can be one of the flags listed in <a href="https://msdn.microsoft.com/a46845bf-ade6-4366-8a73-6dc960fd7722">SHCONTF</a>.


### -param bstrFileSpec






#### - bstrFilter [in]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

A filter string that specifies what should be listed in the <a href="https://msdn.microsoft.com/b99201b3-95e8-4ddd-b338-dee8d107d0a0">FolderItems</a> collection.


## -see-also




<a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a>



<a href="https://msdn.microsoft.com/0ca0efb3-6831-4561-9fd1-6d0b62704931">FolderItems2</a>



<a href="https://msdn.microsoft.com/e8ffe325-e6ae-4fa0-9824-22721c2d97c8">FolderItems3</a>
 

 

