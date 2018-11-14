---
UID: NF:wabapi.IWABObject.VCardDisplay
title: IWABObject::VCardDisplay
author: windows-sdk-content
description: Displays properties on a vCard file.
old-location: wab\_wab_IWABObject_VCardDisplay.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\vcarddisplay.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWABObject interface [Windows Address Book],VCardDisplay method, IWABObject.VCardDisplay, IWABObject::VCardDisplay, VCardDisplay, VCardDisplay method [Windows Address Book], VCardDisplay method [Windows Address Book],IWABObject interface, _wab_IWABObject_VCardDisplay, wab._wab_IWABObject_VCardDisplay, wabapi/IWABObject::VCardDisplay
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
 - IWABObject.VCardDisplay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wabapi.h
: 
- IWABObject.VCardDisplay
: 
req.product: Internet Explorer 4.0
---

# IWABObject::VCardDisplay


## -description


Displays properties on a vCard file.


## -parameters




### -param lpIAB

Type: <b><a href="https://msdn.microsoft.com/df614598-b9ac-462a-89e7-cda0a602c6cd">IAddrBook</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/df614598-b9ac-462a-89e7-cda0a602c6cd">IAddrBook</a> interface 
				that specifies the address book object.


### -param hWnd

Type: <b>HWND</b>

Value of type <b>HWND</b> that specifies 
				the parent window handle for displayed dialog boxes.


### -param lpszFileName

Type: <b>LPSTR</b>

Value of type <b>LPSTR</b> that specifies 		
				the full path of the vCard file to display.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



