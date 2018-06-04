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

# _WABIMPORTPARAM structure


## -description


Do not use. Structure passed to <a href="https://msdn.microsoft.com/88676a07-8b03-4ed3-a5bb-a54a11b093c8">Import</a> that gives information about importing .wab files.


## -struct-fields




### -field cbSize

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies the size of the structure in bytes.


### -field lpAdrBook

Type: <b><a href="https://msdn.microsoft.com/df614598-b9ac-462a-89e7-cda0a602c6cd">IAddrBook</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/df614598-b9ac-462a-89e7-cda0a602c6cd">IAddrBook</a> interface that specifies the address book object to import to.


### -field hWnd

 


### -field ulFlags

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies flags affecting behavior.



#### MAPI_DIALOG

Causes <a href="https://msdn.microsoft.com/88676a07-8b03-4ed3-a5bb-a54a11b093c8">Import</a> to show a dialog box with a progress bar indicating the progress of the import process.


### -field lpszFileName

Type: <b>LPSTR</b>

Value of type <b>LPSTR</b> that specifies the filename to import, or <b>NULL</b> to cause a FileOpen dialog box to open.


#### - hwnd

Type: <b>HWND</b>

Value of type <b>HWND</b> that specifies the parent window handle for any dialog boxes.

