---
UID: NS:wabapi._WABIMPORTPARAM
title: "_WABIMPORTPARAM"
author: windows-sdk-content
description: Do not use. Structure passed to Import that gives information about importing .wab files.
old-location: wab\_wab_WABIMPORTPARAM.htm
old-project: wab
ms.assetid: VS|wab|~\wab\reference\structures\wabimportparam.htm
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*LPWABIMPORTPARAM, LPWABIMPORTPARAM, LPWABIMPORTPARAM structure pointer [Windows Address Book], MAPI_DIALOG, WABIMPORTPARAM, WABIMPORTPARAM structure [Windows Address Book], _WABIMPORTPARAM, _wab_WABIMPORTPARAM, wab._wab_WABIMPORTPARAM, wabapi/LPWABIMPORTPARAM, wabapi/WABIMPORTPARAM"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: WABIMPORTPARAM, *LPWABIMPORTPARAM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wabapi.h
api_name:
-	WABIMPORTPARAM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
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

