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

# ITransferAdviseSink::UpdateProgress


## -description


Updates the transfer progress status in the UI.


## -parameters




### -param ullSizeCurrent [in]

Type: <b>ULONGLONG</b>

The number of bytes processed in the current operation.


### -param ullSizeTotal [in]

Type: <b>ULONGLONG</b>

The total number of bytes in the current operation.


### -param nFilesCurrent [in]

Type: <b>int</b>

The number of files processed in the current operation.


### -param nFilesTotal [in]

Type: <b>int</b>

The total number of files in the operation. Set to 0 to indicate that the value has not changed since the last call to this method.


### -param nFoldersCurrent [in]

Type: <b>int</b>

The number of folders processed in the current operation.


### -param nFoldersTotal [in]

Type: <b>int</b>

The total number of folders in the operation. Set to 0 to indicate that the value has not changed since the last call to this method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Set <i>ullSizeTotal</i>, <i>nFilesTotal</i>, and <i>nFoldersTotal</i> all to 0 to indicate that the totals have not changed since the last call to this method.

Set all six parameters to 0 to indicate that progress has not changed since the last call to this method.

<h3><a id="Note_to_Implementers"></a><a id="note_to_implementers"></a><a id="NOTE_TO_IMPLEMENTERS"></a>Note to Implementers</h3>
Implementers of this function should return an erorr code when the operation needs to terminate before it is complete, such as when the user clicks the <b>Cancel</b> button.



