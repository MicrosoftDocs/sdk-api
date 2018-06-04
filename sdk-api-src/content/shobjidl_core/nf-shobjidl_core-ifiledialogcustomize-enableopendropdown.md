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

# IFileDialogCustomize::EnableOpenDropDown


## -description


Enables a drop-down list on the <b>Open</b> or <b>Save</b> button in the dialog.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the drop-down list.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Open or Save button label takes on the text of the first item in the drop-down. This overrides any label set by <a href="https://msdn.microsoft.com/4320de0f-bfa6-4e17-a09d-d004559fae70">IFileDialog::SetOkButtonLabel</a>.

 Use <a href="https://msdn.microsoft.com/56d7d0df-0c3e-4bc3-b91e-3b191f5dad76">IFileDialogCustomize::AddControlItem</a> to add items to the drop-down.



