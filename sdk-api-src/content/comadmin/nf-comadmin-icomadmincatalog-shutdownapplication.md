---
UID: NF:comadmin.ICOMAdminCatalog.ShutdownApplication
title: ICOMAdminCatalog::ShutdownApplication
author: windows-sdk-content
description: Initiates shutdown of a COM+ server application process.
old-location: cos\icomadmincatalog_shutdownapplication.htm
old-project: cossdk
ms.assetid: 79f3af18-0924-4e09-85aa-54a6886b65b3
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: ICOMAdminCatalog interface [COM+],ShutdownApplication method, ICOMAdminCatalog.ShutdownApplication, ICOMAdminCatalog::ShutdownApplication, ShutdownApplication, ShutdownApplication method [COM+], ShutdownApplication method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_ShutdownApplication, comadmin/ICOMAdminCatalog::ShutdownApplication, cos.icomadmincatalog_shutdownapplication
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog.ShutdownApplication
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a>
 

 

