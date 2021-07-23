---
UID: NF:shappmgr.IPublishedApp.GetPublishedAppInfo
title: IPublishedApp::GetPublishedAppInfo (shappmgr.h)
description: Gets publishing-related information about an application published by an application publisher.
helpviewer_keywords: ["GetPublishedAppInfo","GetPublishedAppInfo method [Windows Shell]","GetPublishedAppInfo method [Windows Shell]","IPublishedApp interface","IPublishedApp interface [Windows Shell]","GetPublishedAppInfo method","IPublishedApp.GetPublishedAppInfo","IPublishedApp::GetPublishedAppInfo","inet_IPublishedApp_GetPublishedAppInfo","shappmgr/IPublishedApp::GetPublishedAppInfo","shell.IPublishedApp_GetPublishedAppInfo"]
old-location: shell\IPublishedApp_GetPublishedAppInfo.htm
tech.root: shell
ms.assetid: 4ffcc30a-cf07-45e7-b9a5-342fe2b553c8
ms.date: 12/05/2018
ms.keywords: GetPublishedAppInfo, GetPublishedAppInfo method [Windows Shell], GetPublishedAppInfo method [Windows Shell],IPublishedApp interface, IPublishedApp interface [Windows Shell],GetPublishedAppInfo method, IPublishedApp.GetPublishedAppInfo, IPublishedApp::GetPublishedAppInfo, inet_IPublishedApp_GetPublishedAppInfo, shappmgr/IPublishedApp::GetPublishedAppInfo, shell.IPublishedApp_GetPublishedAppInfo
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPublishedApp::GetPublishedAppInfo
 - shappmgr/IPublishedApp::GetPublishedAppInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shappmgr.h
api_name:
 - IPublishedApp.GetPublishedAppInfo
---

# IPublishedApp::GetPublishedAppInfo


## -description

Gets publishing-related information about an application published by an application publisher.

## -parameters

### -param ppai [out]

Type: <b><a href="/windows/desktop/api/shappmgr/ns-shappmgr-pubappinfo">PUBAPPINFO</a>*</b>

A pointer to an <a href="/windows/desktop/api/shappmgr/ns-shappmgr-pubappinfo">PUBAPPINFO</a> structure that returns the application information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The dwMask member of the <a href="/windows/desktop/api/shappmgr/ns-shappmgr-pubappinfo">PUBAPPINFO</a> structure indicates which members have been requested. Note that Add/Remove Programs will not set the PAI_SCHEDULEDTIME and PAI_EXPIREDTIME bits.  However, the corresponding values stScheduled and stExpired will be used when applicable if the implementation provides them.  A publisher should provide this data if it is available.


#### Examples

The example shows a sample implementation:


```cpp
HRESULT CPubApp::GetPublishedAppInfo(PUBAPPINFO *pInfo)
{
    if (sizeof(PUBAPPINFO) != pInfo->cbSize)
        return E_FAIL;
		
    // Add/Remove Programs will use these items but will not ask for them.

    pInfo->dwMask |= (PAI_EXPIRETIME | PAI_SCHEDULEDTIME);

    // First save off the mask of requested data items.

    const DWORD dwMask = pInfo->dwMask;

    // Zero-out the mask.  The bits should be set as items are retrieved.

    pInfo->dwMask = 0;

    // Call an internal function that obtains data and sets
    // bits in pInfo->dwMask for each item obtained.

    return get_pub_app_info(pInfo, dwMask);
}


					
```

## -see-also

<a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ienumpublishedapps">IEnumPublishedApps</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>



<a href="/windows/desktop/api/shappmgr/ns-shappmgr-pubappinfo">PUBAPPINFO</a>