---
UID: NF:wabapi.IWABObject.Import
title: IWABObject::Import
author: windows-sdk-content
description: Imports a .wab file into the user's Address Book.
old-location: wab\_wab_IWABObject_Import.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\import.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWABObject interface [Windows Address Book],Import method, IWABObject.Import, IWABObject::Import, Import, Import method [Windows Address Book], Import method [Windows Address Book],IWABObject interface, _wab_IWABObject_Import, wab._wab_IWABObject_Import, wabapi/IWABObject::Import
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wabapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wab32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IWABObject.Import
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IWABObject::Import


## -description


Imports a .wab file into the user's Address Book.


## -parameters




### -param lpWIP

TBD




#### - lpImportParam

Type: <b>LPSTR</b>

Pointer to a <a href="https://msdn.microsoft.com/fd25ce3f-81cc-42f6-9720-b30c09c75de5">WABIMPORTPARAM</a> 
				structure.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.
			




## -remarks



When calling this method, pass a pointer to a 
	<a href="https://msdn.microsoft.com/fd25ce3f-81cc-42f6-9720-b30c09c75de5">WABIMPORTPARAM</a> structure. If the caller specifies 
	<b>MAPI_DIALOG</b> in the 
	<b>ulFlags</b> member of the structure, 
	the Windows Address Book (WAB) shows a dialog box with a progress bar indicating 
	the progress of the import process. The caller can specify a file name 
	to import. If the caller specifies a <b>NULL</b> file name, the 
	WAB opens a <a href="_win32_GetOpenFileName">GetOpenFileName</a> 
	dialog box to prompt the user to select a .wab file for importing.

For compatibility with previously released versions of the 
	WAB that expose this method, the pointer to the 
	<a href="https://msdn.microsoft.com/fd25ce3f-81cc-42f6-9720-b30c09c75de5">WABIMPORTPARAM</a> structure needs to be cast to an 
	<b>LPSTR</b> prior to passing it into this method.



