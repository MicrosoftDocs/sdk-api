---
UID: NF:shobjidl_core.INewMenuClient.SelectAndEditItem
title: INewMenuClient::SelectAndEditItem (shobjidl_core.h)
description: INewMenuClient::SelectAndEditItem method
helpviewer_keywords: ["INewMenuClient interface [Windows Shell]","SelectAndEditItem method","INewMenuClient.SelectAndEditItem","INewMenuClient::SelectAndEditItem","NMCSAEI_EDIT","NMCSAEI_SELECT","SelectAndEditItem","SelectAndEditItem method [Windows Shell]","SelectAndEditItem method [Windows Shell]","INewMenuClient interface","_shell_INewMenuClient_SelectAndEditItem","shell.INewMenuClient_SelectAndEditItem","shobjidl_core/INewMenuClient::SelectAndEditItem"]
old-location: shell\INewMenuClient_SelectAndEditItem.htm
tech.root: shell
ms.assetid: f731e69f-8ff0-42ff-96f8-04236f53d962
ms.date: 12/05/2018
ms.keywords: INewMenuClient interface [Windows Shell],SelectAndEditItem method, INewMenuClient.SelectAndEditItem, INewMenuClient::SelectAndEditItem, NMCSAEI_EDIT, NMCSAEI_SELECT, SelectAndEditItem, SelectAndEditItem method [Windows Shell], SelectAndEditItem method [Windows Shell],INewMenuClient interface, _shell_INewMenuClient_SelectAndEditItem, shell.INewMenuClient_SelectAndEditItem, shobjidl_core/INewMenuClient::SelectAndEditItem
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
 - INewMenuClient::SelectAndEditItem
 - shobjidl_core/INewMenuClient::SelectAndEditItem
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
 - INewMenuClient.SelectAndEditItem
---

# INewMenuClient::SelectAndEditItem


## -description

Selects or edits the specified item in the menu.

## -parameters

### -param pidlItem [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

### -param flags [in]

Type: <b>NMCSAEI_FLAGS</b>



#### NMCSAEI_SELECT (0x0000)

0x0000. Select the item.



#### NMCSAEI_EDIT (0x0001)

0x0001. Edit the item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

