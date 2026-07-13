---
UID: NF:shappmgr.IShellApp.GetAppInfo
title: IShellApp::GetAppInfo (shappmgr.h)
description: Gets general information about an application.
helpviewer_keywords: ["GetAppInfo","GetAppInfo method [Windows Shell]","GetAppInfo method [Windows Shell]","IShellApp interface","IShellApp interface [Windows Shell]","GetAppInfo method","IShellApp.GetAppInfo","IShellApp::GetAppInfo","inet_IShellApp_GetAppInfo","shappmgr/IShellApp::GetAppInfo","shell.IShellApp_GetAppInfo"]
old-location: shell\IShellApp_GetAppInfo.htm
tech.root: shell
ms.assetid: 8842c12e-2b59-49d6-8140-5a402509a0dd
ms.date: 12/05/2018
ms.keywords: GetAppInfo, GetAppInfo method [Windows Shell], GetAppInfo method [Windows Shell],IShellApp interface, IShellApp interface [Windows Shell],GetAppInfo method, IShellApp.GetAppInfo, IShellApp::GetAppInfo, inet_IShellApp_GetAppInfo, shappmgr/IShellApp::GetAppInfo, shell.IShellApp_GetAppInfo
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellApp::GetAppInfo
 - shappmgr/IShellApp::GetAppInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellApp.GetAppInfo
---

## -description

Gets general information about an application.

## -parameters

### -param pai [out]

Type: **[APPINFODATA](/windows/win32/api/shappmgr/ns-shappmgr-appinfodata)***

A pointer to an [APPINFODATA](/windows/win32/api/shappmgr/ns-shappmgr-appinfodata) structure that returns the application information.

## -returns

Type: **HRESULT**

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

<div class="alert">**Note**  Add/Remove Programs in the Control Panel sets the cbSize and dwMask members of the [APPINFODATA](/windows/win32/api/shappmgr/ns-shappmgr-appinfodata) structure.</div>
<div> </div>

Your implementation should validate cbSize by comparing it with the size of [APPINFODATA](/windows/win32/api/shappmgr/ns-shappmgr-appinfodata). If cbSize does not equal the size of **APPINFODATA**, this method should return a COM error value like E_FAIL.

Add/Remove Programs in the Control Panel will set the dwMask member of the [APPINFODATA](/windows/win32/api/shappmgr/ns-shappmgr-appinfodata) structure to indicate that you should return AIM_DISPLAYNAME and AIM_SUPPORTURL. For each value that you return in APPINFODATA, you must set the corresponding bit in dwMask. All other bits should be cleared.

#### Examples

Here is a sample of how to use the dwMask bits:

```cpp
HRESULT CPubApp::GetAppInfo(APPINFODATA *pData)
{
    if (sizeof(APPINFODATA) != pData->cbSize)
        return E_FAIL;

    // First save off the mask of requested data items.

    const DWORD dwMask = pData->dwMask;

    // Zero-out the mask.  Bits will be set as items are obtained. 

    pData->dwMask = 0;

    // Call an internal function that obtains data and sets
    // bits in pData->dwMask for each item obtained.

    return get_app_info_data(pData, dwMask);
}
```

## -see-also

* [APPINFODATA](/windows/win32/api/shappmgr/ns-shappmgr-appinfodata)
* [IAppPublisher](/windows/win32/api/shappmgr/nn-shappmgr-iapppublisher)
* [IPublishedApp::GetPublishedAppInfo](/windows/win32/api/shappmgr/nf-shappmgr-ipublishedapp-getpublishedappinfo)
* [IShellApp](/windows/win32/api/shappmgr/nn-shappmgr-ishellapp)
