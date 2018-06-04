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

# IFileDialog::GetFileTypeIndex


## -description


Gets the currently selected file type.


## -parameters




### -param piFileType [out]

Type: <b>UINT*</b>

A pointer to a <b>UINT</b> value that receives the index of the selected file type in the file type array passed to <a href="https://msdn.microsoft.com/ca850988-7f2f-4faf-9ded-14db476fc452">IFileDialog::SetFileTypes</a> in its <i>cFileTypes</i> parameter.

<div class="alert"><b>Note</b>  This is a one-based index rather than zero-based.</div>
<div> </div>

## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IFileDialog::GetFileTypeIndex</b> can be called either while the dialog is open or after it has closed.



