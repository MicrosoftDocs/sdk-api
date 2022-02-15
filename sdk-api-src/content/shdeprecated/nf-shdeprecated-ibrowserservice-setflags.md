---
UID: NF:shdeprecated.IBrowserService.SetFlags
title: IBrowserService::SetFlags (shdeprecated.h)
description: Deprecated. Sets flags that indicate browser status.
helpviewer_keywords: ["BSF_CANMAXIMIZE","BSF_DELEGATEDNAVIGATION","BSF_DONTSHOWNAVCANCELPAGE","BSF_FEEDNAVIGATION","BSF_FEEDSUBSCRIBED","BSF_HTMLNAVCANCELED","BSF_MERGEDMENUS","BSF_NAVNOHISTORY","BSF_NOLOCALFILEWARNING","BSF_REGISTERASDROPTARGET","BSF_RESIZABLE","BSF_SETNAVIGATABLECODEPAGE","BSF_THEATERMODE","BSF_TOPBROWSER","BSF_TRUSTEDFORACTIVEX","BSF_UISETBYAUTOMATION","IBrowserService interface [Windows Shell]","SetFlags method","IBrowserService.SetFlags","IBrowserService::SetFlags","SetFlags","SetFlags method [Windows Shell]","SetFlags method [Windows Shell]","IBrowserService interface","shdeprecated/IBrowserService::SetFlags","shell.IBrowserService_SetFlags","zone_IBrowserService_SetFlags"]
old-location: shell\IBrowserService_SetFlags.htm
tech.root: shell
ms.assetid: 696d4350-95f9-4d69-bb4b-92f4c26b3f65
ms.date: 12/05/2018
ms.keywords: BSF_CANMAXIMIZE, BSF_DELEGATEDNAVIGATION, BSF_DONTSHOWNAVCANCELPAGE, BSF_FEEDNAVIGATION, BSF_FEEDSUBSCRIBED, BSF_HTMLNAVCANCELED, BSF_MERGEDMENUS, BSF_NAVNOHISTORY, BSF_NOLOCALFILEWARNING, BSF_REGISTERASDROPTARGET, BSF_RESIZABLE, BSF_SETNAVIGATABLECODEPAGE, BSF_THEATERMODE, BSF_TOPBROWSER, BSF_TRUSTEDFORACTIVEX, BSF_UISETBYAUTOMATION, IBrowserService interface [Windows Shell],SetFlags method, IBrowserService.SetFlags, IBrowserService::SetFlags, SetFlags, SetFlags method [Windows Shell], SetFlags method [Windows Shell],IBrowserService interface, shdeprecated/IBrowserService::SetFlags, shell.IBrowserService_SetFlags, zone_IBrowserService_SetFlags
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService::SetFlags
 - shdeprecated/IBrowserService::SetFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService.SetFlags
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

