---
UID: NF:shobjidl_core.IFolderFilterSite.SetFilter
title: IFolderFilterSite::SetFilter
author: windows-sdk-content
description: Exposed by a host to allow clients to pass the host their IUnknown interface pointers.
old-location: shell\IFolderFilterSite_SetFilter.htm
old-project: shell
ms.assetid: 1bbcb238-9b3e-4f5c-9cb3-429d0ff918af
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IFolderFilterSite interface [Windows Shell],SetFilter method, IFolderFilterSite.SetFilter, IFolderFilterSite::SetFilter, SetFilter, SetFilter method [Windows Shell], SetFilter method [Windows Shell],IFolderFilterSite interface, _shell_IFolderFilterSite_SetFilter, shell.IFolderFilterSite_SetFilter, shobjidl_core/IFolderFilterSite::SetFilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Shell32.dll
api_name:
 - IFolderFilterSite.SetFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IFolderFilterSite::SetFilter


## -description


Exposed by a host to allow clients to pass the host their <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface pointers.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the client's <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. To notify the host to terminate filtering and stop calling your <a href="https://msdn.microsoft.com/fd69c11c-f4c3-4681-ae85-385460e96be9">IFolderFilter</a> interface, set this parameter to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After you get a pointer to the host's <a href="https://msdn.microsoft.com/8b6fe1a3-9977-42a8-af95-da0fc6809b1b">IFolderFilterSite</a> interface, call this method to pass the host a pointer to your <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. The host will then use this pointer to call your <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method to request a pointer to your <a href="https://msdn.microsoft.com/fd69c11c-f4c3-4681-ae85-385460e96be9">IFolderFilter</a> interface. If this call fails, <b>IFolderFilterSite::SetFilter</b> returns <b>E_NOINTERFACEAVAILABLE</b>. If the call is successful, the host will then call the <b>IFolderFilter</b> interface's two methods to determine how to enumerate the contents of the folder.



