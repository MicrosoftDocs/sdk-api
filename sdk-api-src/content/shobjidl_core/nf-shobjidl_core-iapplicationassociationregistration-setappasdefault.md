---
UID: NF:shobjidl_core.IApplicationAssociationRegistration.SetAppAsDefault
title: IApplicationAssociationRegistration::SetAppAsDefault (shobjidl_core.h)
author: windows-sdk-content
description: Sets an application as the default for a given type. For more information, see Default Programs. Not intended for use in Windows 8.
old-location: shell\IApplicationAssociationRegistration_SetAppAsDefault.htm
tech.root: shell
ms.assetid: 30870adb-793f-404f-809c-1ec34a1f6b82
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IApplicationAssociationRegistration interface [Windows Shell],SetAppAsDefault method, IApplicationAssociationRegistration.SetAppAsDefault, IApplicationAssociationRegistration::SetAppAsDefault, SetAppAsDefault, SetAppAsDefault method [Windows Shell], SetAppAsDefault method [Windows Shell],IApplicationAssociationRegistration interface, _shell_IApplicationAssociationRegistration_SetAppAsDefault, shell.IApplicationAssociationRegistration_SetAppAsDefault, shobjidl_core/IApplicationAssociationRegistration::SetAppAsDefault
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IApplicationAssociationRegistration.SetAppAsDefault"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IApplicationAssociationRegistration.SetAppAsDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IApplicationAssociationRegistration::SetAppAsDefault


## -description


Sets an application as the default for a given type. For more information, see <a href="https://docs.microsoft.com/windows/desktop/shell/default-programs">Default Programs</a>. Not intended for use in Windows 8.


## -parameters




### -param pszAppRegistryName [in]

Type: <b>LPCWSTR</b>

A pointer to a <b>null</b>-terminated Unicode string that specifies the registered name of the application.


### -param pszSet [in]

Type: <b>LPCWSTR</b>

A pointer to a <b>null</b>-terminated Unicode string that contains the file name extension or protocol of the application, such as .mp3 or http.


### -param atSetType [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype">ASSOCIATIONTYPE</a></b>

One of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype">ASSOCIATIONTYPE</a> enumeration values that specifies the type of the application named in <i>pszSet</i>, such as file name extension or MIME type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/shell/default-programs">Default Programs</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration">IApplicationAssociationRegistration</a>
 

 

