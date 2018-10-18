---
UID: NF:shobjidl_core.IApplicationAssociationRegistration.QueryAppIsDefaultAll
title: IApplicationAssociationRegistration::QueryAppIsDefaultAll
author: windows-sdk-content
description: Determines whether an application owns all of the registered default associations for a given application level. Not intended for use in Windows 8.
old-location: shell\IApplicationAssociationRegistration_QueryAppIsDefaultAll.htm
tech.root: shell
ms.assetid: 71073f30-51bc-4522-9bb2-7eb743bca159
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IApplicationAssociationRegistration interface [Windows Shell],QueryAppIsDefaultAll method, IApplicationAssociationRegistration.QueryAppIsDefaultAll, IApplicationAssociationRegistration::QueryAppIsDefaultAll, QueryAppIsDefaultAll, QueryAppIsDefaultAll method [Windows Shell], QueryAppIsDefaultAll method [Windows Shell],IApplicationAssociationRegistration interface, _shell_IApplicationAssociationRegistration_QueryAppIsDefaultAll, shell.IApplicationAssociationRegistration_QueryAppIsDefaultAll, shobjidl_core/IApplicationAssociationRegistration::QueryAppIsDefaultAll
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
 - IApplicationAssociationRegistration.QueryAppIsDefaultAll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IApplicationAssociationRegistration::QueryAppIsDefaultAll


## -description


Determines whether an application owns all of the registered default associations for a given application level. Not intended for use in Windows 8.


## -parameters




### -param alQueryLevel [in]

Type: <b><a href="https://msdn.microsoft.com/846ce9f4-092a-420d-be73-0951efc4368f">ASSOCIATIONLEVEL</a></b>

One of the <a href="https://msdn.microsoft.com/846ce9f4-092a-420d-be73-0951efc4368f">ASSOCIATIONLEVEL</a> enumeration values that specifies the level of association, such as per-user or machine. This is typically <a href="https://msdn.microsoft.com/846ce9f4-092a-420d-be73-0951efc4368f">AL_EFFECTIVE</a>.


### -param pszAppRegistryName [in]

Type: <b>LPCWSTR</b>

A pointer to a <b>null</b>-terminated Unicode string that specifies the registered name of the application.


### -param pfDefault [out]

Type: <b>BOOL*</b>

When this method returns, contains <b>TRUE</b> if the application is the default for all <a href="https://msdn.microsoft.com/3dbbe748-5e83-4103-932a-b51a2a55f9fd"> association types</a> at the specified <a href="https://msdn.microsoft.com/846ce9f4-092a-420d-be73-0951efc4368f">ASSOCIATIONLEVEL</a>; 
or <b>FALSE</b> otherwise.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/78cd05a4-df33-42b5-91b9-826ebce04a1d">Default Programs</a>



<a href="https://msdn.microsoft.com/015a3be4-2e74-4a2b-8c02-54dcbf0ecacd">IApplicationAssociationRegistration</a>
 

 

