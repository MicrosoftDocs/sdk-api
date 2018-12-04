---
UID: NF:wabapi.IWABObject.Find
title: IWABObject::Find
author: windows-sdk-content
description: Launches the Windows Address Book (WAB) Find dialog box.
old-location: wab\_wab_IWABObject_Find.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\find.htm
ms.author: windowssdkdev
ms.date: 11/28/2018
ms.keywords: Find, Find method [Windows Address Book], Find method [Windows Address Book],IWABObject interface, IWABObject interface [Windows Address Book],Find method, IWABObject.Find, IWABObject::Find, _wab_IWABObject_Find, wab._wab_IWABObject_Find, wabapi/IWABObject::Find
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
 - IWABObject.Find
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5
---

# IWABObject::Find


## -description


Launches the Windows Address Book (WAB) Find dialog box.


## -parameters




### -param lpIAB

Type: <b><a href="https://msdn.microsoft.com/df614598-b9ac-462a-89e7-cda0a602c6cd">IAddrBook</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/df614598-b9ac-462a-89e7-cda0a602c6cd">IAddrBook</a> interface 
				that specifies the address book to search.


### -param hWnd

Type: <b>HWND</b>

Value of type <b>HWND</b> that specifies 
				the handle to the parent window for the Find dialog box. 
				The value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful.
			



