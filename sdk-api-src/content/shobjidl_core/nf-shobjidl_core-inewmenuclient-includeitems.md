---
UID: NF:shobjidl_core.INewMenuClient.IncludeItems
title: INewMenuClient::IncludeItems (shobjidl_core.h)
description: Allows the view to filter the items shown in the menu.
helpviewer_keywords: ["INewMenuClient interface [Windows Shell]","IncludeItems method","INewMenuClient.IncludeItems","INewMenuClient::IncludeItems","IncludeItems","IncludeItems method [Windows Shell]","IncludeItems method [Windows Shell]","INewMenuClient interface","NMCII_FOLDERS","NMCII_ITEMS","NMCII_NONE","_shell_INewMenuClient_IncludeItems","shell.INewMenuClient_IncludeItems","shobjidl_core/INewMenuClient::IncludeItems"]
old-location: shell\INewMenuClient_IncludeItems.htm
tech.root: shell
ms.assetid: 666bf93c-cc99-4530-852e-5ef05ea72348
ms.date: 12/05/2018
ms.keywords: INewMenuClient interface [Windows Shell],IncludeItems method, INewMenuClient.IncludeItems, INewMenuClient::IncludeItems, IncludeItems, IncludeItems method [Windows Shell], IncludeItems method [Windows Shell],INewMenuClient interface, NMCII_FOLDERS, NMCII_ITEMS, NMCII_NONE, _shell_INewMenuClient_IncludeItems, shell.INewMenuClient_IncludeItems, shobjidl_core/INewMenuClient::IncludeItems
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INewMenuClient::IncludeItems
 - shobjidl_core/INewMenuClient::IncludeItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - INewMenuClient.IncludeItems
---

# INewMenuClient::IncludeItems


## -description

Allows the view to filter the items shown in the menu.

## -parameters

### -param pflags [out]

Type: <b>NMCII_FLAGS*</b>

Pointer to a value that, when this method returns successfully, contains one of the following values:



#### NMCII_NONE (0x0000)

0x0000.



#### NMCII_ITEMS (0x0001)

0x0001. Non-folder items.



#### NMCII_FOLDERS (0x0002)

0x0002. Folder items.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

