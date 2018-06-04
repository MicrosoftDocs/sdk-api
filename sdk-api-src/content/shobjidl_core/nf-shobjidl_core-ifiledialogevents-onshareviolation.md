---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFileDialogEvents::OnShareViolation


## -description


Enables an application to respond to sharing violations that arise from Open or Save operations.


## -parameters




### -param pfd [in]

Type: <b><a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a>*</b>

A pointer to the interface that represents the dialog.


### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the interface that represents the item that has the sharing violation.


### -param pResponse [out]

Type: <b><a href="https://msdn.microsoft.com/976965f5-7806-41de-b1d4-f5bb6dc4f79b">FDE_SHAREVIOLATION_RESPONSE</a>*</b>

A pointer to a value from the <a href="https://msdn.microsoft.com/976965f5-7806-41de-b1d4-f5bb6dc4f79b">FDE_SHAREVIOLATION_RESPONSE</a> enumeration indicating the response to the sharing violation.


## -returns



Type: <b>HRESULT</b>

The implementer should return E_NOTIMPL if this method is not implemented; S_OK or an appropriate error code otherwise.




## -remarks



The <b>FOS_SHAREAWARE</b> flag must be set through <a href="https://msdn.microsoft.com/99def5c2-3fc3-416c-80a6-6009927ab63e">IFileDialog::SetOptions</a> before this method is called.

A sharing violation could possibly arise when the application attempts to open a file, because the file could have been locked between the time that the dialog tested it and the application opened it.



