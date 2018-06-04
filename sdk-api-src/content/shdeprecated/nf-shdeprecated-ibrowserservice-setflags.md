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

# IBrowserService::SetFlags


## -description


Deprecated. Sets flags that indicate browser status.


## -parameters




### -param dwFlags

Type: <b>DWORD</b>

A bitmask used in conjunction with the flags indicated in <i>dwFlagMask</i>. For each <i>dwFlagMask</i> bit, the corresponding bit in this value sets (1) or disables (0) that state.


### -param dwFlagMask

Type: <b>DWORD</b>

One or more of the following values.



#### BSF_REGISTERASDROPTARGET (0x00000001)

The browser is registered as a drop target for navigation.



#### BSF_THEATERMODE (0x00000002)

The browser is in theater mode. <b>Not supported by</b>:      Internet Explorer 7 or Windows Vista



#### BSF_NOLOCALFILEWARNING (0x00000010)

Display a no local file warning.



#### BSF_UISETBYAUTOMATION (0x00000100)

The browser's UI is set by automation.



#### BSF_RESIZABLE (0x00000200)

The browser can be resized. <b>Not supported by </b>: Internet Explorer 7 or Windows Vista



#### BSF_CANMAXIMIZE (0x00000400)

The browser can be maximized. <b>Not supported by </b>: Internet Explorer 7 or Windows Vista



#### BSF_TOPBROWSER (0x00000800)

The browser is the top browser window.



#### BSF_NAVNOHISTORY (0x00001000)

The current location should be added to the history.



#### BSF_HTMLNAVCANCELED (0x00002000)

Navigation was canceled.



#### BSF_DONTSHOWNAVCANCELPAGE (0x00004000)

Do not display a page explaining that the navigation was canceled.



#### BSF_SETNAVIGATABLECODEPAGE (0x00008000)

Set a navigable code page.



#### BSF_DELEGATEDNAVIGATION (0x00010000)

Navigation has been delegated.



#### BSF_TRUSTEDFORACTIVEX (0x00020000)

Trust ActiveX objects.



#### BSF_MERGEDMENUS (0x00040000)

0x00040000. 0x00040000. Indicates that this browser instance has merged menus. <b> Not supported by</b>: Internet Explorer 7 or Windows Vista.



#### BSF_FEEDNAVIGATION (0x00080000)

0x00080000. Set on navigation to a feed.



#### BSF_FEEDSUBSCRIBED (0x00100000)

0x00100000. Set on navigation to a subscribed feed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



