---
UID: NF:comadmin.ICOMAdminCatalog2.QueryApplicationFile2
title: ICOMAdminCatalog2::QueryApplicationFile2
author: windows-sdk-content
description: Retrieves information about an application that is about to be installed.
old-location: cos\icomadmincatalog2_queryapplicationfile2.htm
tech.root: cossdk
ms.assetid: 8b2f9ce5-f2d8-4359-ac58-5069d6d58bb7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICOMAdminCatalog2 interface [COM+],QueryApplicationFile2 method, ICOMAdminCatalog2.QueryApplicationFile2, ICOMAdminCatalog2::QueryApplicationFile2, QueryApplicationFile2, QueryApplicationFile2 method [COM+], QueryApplicationFile2 method [COM+],ICOMAdminCatalog2 interface, _cos_icomadmincatalog2_QueryApplicationFile2, comadmin/ICOMAdminCatalog2::QueryApplicationFile2, cos.icomadmincatalog2_queryapplicationfile2
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ICOMAdminCatalog2.QueryApplicationFile2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICOMAdminCatalog2::QueryApplicationFile2


## -description


Retrieves information about an application that is about to be installed.


## -parameters




### -param bstrApplicationFile [in]

The full path to the application file.


### -param ppFilesForImport [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/7c24ead4-d69f-467d-b3d8-a81adbc49a7b">ICatalogCollection</a> interface pointer that specifies the <a href="https://msdn.microsoft.com/9ed4bc3f-3490-4c36-ba94-bc803886a4d2">FilesForImport</a> collection for the application.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/ffca611d-dacc-47be-9101-9de76ecc8393">ICOMAdminCatalog2</a>
 

 

