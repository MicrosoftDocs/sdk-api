---
UID: NF:wabapi.IWABObject.SetMe
title: IWABObject::SetMe
author: windows-sdk-content
description: Designates a particular contact as the ME object.
old-location: wab\_wab_IWABObject_SetMe.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\setme.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWABObject interface [Windows Address Book],SetMe method, IWABObject.SetMe, IWABObject::SetMe, MAPI_DIALOG, SetMe, SetMe method [Windows Address Book], SetMe method [Windows Address Book],IWABObject interface, _wab_IWABObject_SetMe, wab._wab_IWABObject_SetMe, wabapi/IWABObject::SetMe
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
 - IWABObject.SetMe
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IWABObject::SetMe


## -description


Designates a particular contact as the ME object.


## -parameters




### -param lpIAB

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms629649(v=VS.85).aspx">IAddrBook</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms629649(v=VS.85).aspx">IAddrBook</a> interface 
				that specifies the address book.


### -param ulFlags

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies flags 
				affecting behavior.



#### MAPI_DIALOG

Causes a selection dialog box to be displayed.


### -param sbEID

Type: <b><a href="https://msdn.microsoft.com/library/ms528837(v=EXCHG.10).aspx">SBinary</a></b>

Value of type <a href="https://msdn.microsoft.com/library/ms528837(v=EXCHG.10).aspx">SBinary</a> that 
				specifies the entry identifier of the contact that should be tagged 
				as ME.


### -param hwnd

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies the 
				parent window handle for displaying dialog boxes. Cast the 
				parent <b>HWND</b> to a <b>ULONG</b> 
				before passing.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error code otherwise.




## -remarks



If the calling application provides an entry identifier to set as the ME object,
	 and <i>ulFlags</i> is set to zero, the entry corresponding 
	 to the entry identifier is designated as "ME" and any previous ME entry is cleared 
	 of this setting.

If the calling application specifies 
<b>MAPI_DIALOG</b> in the <i>ulFlags</i> parameter,
 the Windows Address Book (WAB) displays a ME selection dialog box which contains 
 a list of contacts from which the user can choose. If the application passed 
 in an entry identifier, the entry corresponding to the entry identifier is pre-selected 
 in the contact list. If the application did not pass in an entry identifier, 
 and a ME entry currently exists in the WAB, the current ME entry is 
 pre-selected in the contact list.

Passing a combination of no flags and no entry identifiers is not valid.



