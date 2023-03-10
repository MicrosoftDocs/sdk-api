---
UID: NF:shobjidl_core.IFolderViewSettings.GetColumnPropertyList
title: IFolderViewSettings::GetColumnPropertyList (shobjidl_core.h)
description: Gets an ordered list of columns that corresponds to the column enumerated.
helpviewer_keywords: ["GetColumnPropertyList","GetColumnPropertyList method [Windows Shell]","GetColumnPropertyList method [Windows Shell]","IFolderViewSettings interface","IFolderViewSettings interface [Windows Shell]","GetColumnPropertyList method","IFolderViewSettings.GetColumnPropertyList","IFolderViewSettings::GetColumnPropertyList","_shell_IFolderViewSettings_GetColumnPropertyList","shell.IFolderViewSettings_GetColumnPropertyList","shobjidl_core/IFolderViewSettings::GetColumnPropertyList"]
old-location: shell\IFolderViewSettings_GetColumnPropertyList.htm
tech.root: shell
ms.assetid: 30678ace-e6b2-4655-b92f-fc8a1899e3e0
ms.date: 12/05/2018
ms.keywords: GetColumnPropertyList, GetColumnPropertyList method [Windows Shell], GetColumnPropertyList method [Windows Shell],IFolderViewSettings interface, IFolderViewSettings interface [Windows Shell],GetColumnPropertyList method, IFolderViewSettings.GetColumnPropertyList, IFolderViewSettings::GetColumnPropertyList, _shell_IFolderViewSettings_GetColumnPropertyList, shell.IFolderViewSettings_GetColumnPropertyList, shobjidl_core/IFolderViewSettings::GetColumnPropertyList
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFolderViewSettings::GetColumnPropertyList
 - shobjidl_core/IFolderViewSettings::GetColumnPropertyList
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
 - IFolderViewSettings.GetColumnPropertyList
---

# IFolderViewSettings::GetColumnPropertyList


## -description

Gets an ordered list of columns that corresponds to the column enumerated.

## -parameters

### -param riid

A reference to the interface identifier (IID) of the IPropertyDescriptionList.

### -param ppv

Type: <b><a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a>**</b>

The address of an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.