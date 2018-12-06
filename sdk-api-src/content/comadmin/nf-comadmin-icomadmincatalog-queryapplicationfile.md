---
UID: NF:comadmin.ICOMAdminCatalog.QueryApplicationFile
title: ICOMAdminCatalog::QueryApplicationFile
author: windows-sdk-content
description: Retrieves information about a COM+ application from an application file.
old-location: cos\icomadmincatalog_queryapplicationfile.htm
tech.root: cossdk
ms.assetid: 5f90da9d-06eb-4ec0-8ea1-d040c8e084b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICOMAdminCatalog interface [COM+],QueryApplicationFile method, ICOMAdminCatalog.QueryApplicationFile, ICOMAdminCatalog::QueryApplicationFile, QueryApplicationFile, QueryApplicationFile method [COM+], QueryApplicationFile method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_QueryApplicationFile, comadmin/ICOMAdminCatalog::QueryApplicationFile, cos.icomadmincatalog_queryapplicationfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
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
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog.QueryApplicationFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICOMAdminCatalog::QueryApplicationFile


## -description


Retrieves information about a COM+ application from an application file.


## -parameters




### -param bstrApplicationFile [in]

The application file from which information is to be retrieved.


### -param pbstrApplicationName [out]

The application name in the specified file.


### -param pbstrApplicationDescription [out]

The application description.


### -param pbHasUsers [out]

Indicates whether the application has user information associated with its roles.


### -param pbIsProxy [out]

Indicates whether the file contains an application proxy.


### -param ppsaVarFileNames [out]

An array of names of the DLL files for the components installed in the application.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a>
 

 

