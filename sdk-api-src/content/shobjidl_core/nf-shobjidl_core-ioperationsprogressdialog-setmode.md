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

# IOperationsProgressDialog::SetMode


## -description


Sets progress dialog operations mode.


## -parameters




### -param mode [in]

Type: <b>PDMODE</b>

Specifies the operation mode. The following are valid values.



#### PDM_DEFAULT

0x00000000. Use the default progress dialog operations mode.



#### PDM_RUN

0x00000001. The operation is running.



#### PDM_PREFLIGHT

0x00000002. The operation is gathering data before it begins, such as calculating the predicted operation time.



#### PDM_UNDOING

0x00000004. The operation is rolling back due to an Undo command from the user.



#### PDM_ERRORSBLOCKING

0x00000008. Error dialogs are blocking progress from continuing.



#### PDM_INDETERMINATE

0x00000010. The length of the operation is indeterminate. Do not show a timer and display the progress bar in marquee mode.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



