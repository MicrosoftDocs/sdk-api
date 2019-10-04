---
UID: NF:comadmin.ICOMAdminCatalog.ShutdownApplication
title: ICOMAdminCatalog::ShutdownApplication (comadmin.h)
author: windows-sdk-content
description: Initiates shutdown of a COM+ server application process.
old-location: cos\icomadmincatalog_shutdownapplication.htm
tech.root: cossdk
ms.assetid: 79f3af18-0924-4e09-85aa-54a6886b65b3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICOMAdminCatalog interface [COM+],ShutdownApplication method, ICOMAdminCatalog.ShutdownApplication, ICOMAdminCatalog::ShutdownApplication, ShutdownApplication, ShutdownApplication method [COM+], ShutdownApplication method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_ShutdownApplication, comadmin/ICOMAdminCatalog::ShutdownApplication, cos.icomadmincatalog_shutdownapplication
ms.topic: method
f1_keywords: 
 - "comadmin/ICOMAdminCatalog.ShutdownApplication"
dev_langs:
 - c++
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
 - ICOMAdminCatalog.ShutdownApplication
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICOMAdminCatalog::ShutdownApplication


## -description


Initiates shutdown of a COM+ server application process.


## -parameters




### -param bstrApplIDOrName [in]

The GUID or name of the application.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMADMIN_E_OBJECT_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The application does not exist.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>
 

 

