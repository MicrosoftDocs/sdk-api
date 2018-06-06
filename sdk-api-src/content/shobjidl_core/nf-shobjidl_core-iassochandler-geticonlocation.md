---
UID: NF:shobjidl_core.IAssocHandler.GetIconLocation
title: IAssocHandler::GetIconLocation
author: windows-sdk-content
description: Retrieves the location of the icon associated with the application.
old-location: shell\IAssocHandler_GetIconLocation.htm
old-project: shell
ms.assetid: 4b883c2c-6845-4e53-b41b-83c09091ee53
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetIconLocation, GetIconLocation method [Windows Shell], GetIconLocation method [Windows Shell],IAssocHandler interface, IAssocHandler interface [Windows Shell],GetIconLocation method, IAssocHandler.GetIconLocation, IAssocHandler::GetIconLocation, _shell_IAssocHandler_GetIconLocation, shell.IAssocHandler_GetIconLocation, shobjidl_core/IAssocHandler::GetIconLocation
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
 - IAssocHandler.GetIconLocation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IAssocHandler::GetIconLocation


## -description


Retrieves the location of the icon associated with the application.


## -parameters




### -param ppszPath [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated, Unicode string that contains the path to the application's icon.


### -param pIndex [out]

Type: <b>int*</b>

When this method returns, contains a pointer to the index of the icon within the resource named in <i>ppszPath</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the icon cannot be found, the function will return the path to the executable, and an icon index of zero.

For performance reasons, an application may use the Shell image cache to retrieve the icon, rather than loading the icon directly from the path returned.  The path and icon index can be passed directly to <a href="https://msdn.microsoft.com/f0d4dd1f-a41c-4dd0-9713-e3aec48ff101">Shell_GetCachedImageIndex</a>. One benefit of this is that the Shell cache can provide a default icon in the event that no icon was available for the application.



