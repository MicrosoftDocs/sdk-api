---
UID: NF:shobjidl.IResultsFolder.RemoveIDList
title: IResultsFolder::RemoveIDList
author: windows-sdk-content
description: Removes a pointer to an item identifier list (PIDL) from a results folder.
old-location: shell\IResultsFolder_RemoveIDList.htm
old-project: shell
ms.assetid: 188d4f7f-954c-4bba-ad4e-164085e0cc5a
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IResultsFolder interface [Windows Shell],RemoveIDList method, IResultsFolder.RemoveIDList, IResultsFolder::RemoveIDList, RemoveIDList, RemoveIDList method [Windows Shell], RemoveIDList method [Windows Shell],IResultsFolder interface, _shell_IResultsFolder_RemoveIDList, shell.IResultsFolder_RemoveIDList, shobjidl/IResultsFolder::RemoveIDList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl.h
req.include-header: 
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
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IResultsFolder.RemoveIDList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IResultsFolder::RemoveIDList


## -description


Removes a pointer to an item identifier list (PIDL) from a results folder.


## -parameters




### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL relative to the Desktop.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



