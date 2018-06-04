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

# IFileDialog2::SetCancelButtonLabel


## -description


Replaces the default text "Cancel" on the common file dialog's <b>Cancel</b> button.


## -parameters




### -param pszLabel [in]

Type: <b>LPCWSTR</b>

Pointer to a string that contains the new text to display on the button.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Changing the text on the Cancel button can be useful for situations where the IFileDialogEvents::OnFileOk method is used to accumulate items, and the button text should be Done instead of Cancel, for example.




## -see-also




<a href="https://msdn.microsoft.com/be67a020-285d-4c1e-a8b5-8e1e90fae594">IFileDialog2</a>
 

 

