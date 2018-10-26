---
UID: NF:shobjidl_core.IApplicationAssociationRegistration.SetAppAsDefault
title: IApplicationAssociationRegistration::SetAppAsDefault
author: windows-sdk-content
description: Sets an application as the default for a given type. For more information, see Default Programs. Not intended for use in Windows 8.
old-location: shell\IApplicationAssociationRegistration_SetAppAsDefault.htm
tech.root: shell
ms.assetid: 30870adb-793f-404f-809c-1ec34a1f6b82
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IApplicationAssociationRegistration interface [Windows Shell],SetAppAsDefault method, IApplicationAssociationRegistration.SetAppAsDefault, IApplicationAssociationRegistration::SetAppAsDefault, SetAppAsDefault, SetAppAsDefault method [Windows Shell], SetAppAsDefault method [Windows Shell],IApplicationAssociationRegistration interface, _shell_IApplicationAssociationRegistration_SetAppAsDefault, shell.IApplicationAssociationRegistration_SetAppAsDefault, shobjidl_core/IApplicationAssociationRegistration::SetAppAsDefault
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# IApplicationAssociationRegistration::SetAppAsDefault


## -description


Sets an application as the default for a given type. For more information, see <a href="https://msdn.microsoft.com/78cd05a4-df33-42b5-91b9-826ebce04a1d">Default Programs</a>. Not intended for use in Windows 8.


## -parameters




### -param pszAppRegistryName [in]

Type: <b>LPCWSTR</b>

A pointer to a <b>null</b>-terminated Unicode string that specifies the registered name of the application.


### -param pszSet [in]

Type: <b>LPCWSTR</b>

A pointer to a <b>null</b>-terminated Unicode string that contains the file name extension or protocol of the application, such as .mp3 or http.


### -param atSetType [in]

Type: <b><a href="https://msdn.microsoft.com/3dbbe748-5e83-4103-932a-b51a2a55f9fd">ASSOCIATIONTYPE</a></b>

One of the <a href="https://msdn.microsoft.com/3dbbe748-5e83-4103-932a-b51a2a55f9fd">ASSOCIATIONTYPE</a> enumeration values that specifies the type of the application named in <i>pszSet</i>, such as file name extension or MIME type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/78cd05a4-df33-42b5-91b9-826ebce04a1d">Default Programs</a>



<a href="https://msdn.microsoft.com/015a3be4-2e74-4a2b-8c02-54dcbf0ecacd">IApplicationAssociationRegistration</a>
 

 

