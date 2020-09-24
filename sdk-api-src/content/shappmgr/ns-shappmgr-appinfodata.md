---
UID: NS:shappmgr._AppInfoData
title: APPINFODATA (shappmgr.h)
description: Provides information about a published application to the Add/Remove Programs Control Panel utility.
helpviewer_keywords: ["*PAPPINFODATA","APPINFODATA","APPINFODATA structure [Windows Shell]","inet_APPINFODATA","shappmgr/APPINFODATA","shell.APPINFODATA"]
old-location: shell\APPINFODATA.htm
tech.root: shell
ms.assetid: 3560b088-d899-4fb2-a47c-101f8f5e3bf7
ms.date: 12/05/2018
ms.keywords: '*PAPPINFODATA, APPINFODATA, APPINFODATA structure [Windows Shell], inet_APPINFODATA, shappmgr/APPINFODATA, shell.APPINFODATA'
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
req.typenames: APPINFODATA, *PAPPINFODATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AppInfoData
 - shappmgr/_AppInfoData
 - PAPPINFODATA
 - shappmgr/PAPPINFODATA
 - APPINFODATA
 - shappmgr/APPINFODATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shappmgr.h
api_name:
 - APPINFODATA
---

# APPINFODATA structure


## -description

Provides information about a published application to the Add/Remove Programs Control Panel utility.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

A value of type <b>DWORD</b> that specifies the size of the <b>APPINFODATA</b> data structure. This field is set by the Add/Remove Program executable code.

### -field dwMask

Type: <b>DWORD</b>

A value of type <b>DWORD</b> that specifies the bitmask that indicates which items in the structure are desired or valid. Implementations of <a href="/windows/desktop/api/shappmgr/nf-shappmgr-ishellapp-getappinfo">GetAppInfo</a> should inspect this value for bits that are set and attempt to provide values corresponding to those bits. Implementations should also return with bits set for only those members that are being returned.

### -field pszDisplayName

Type: <b>LPWSTR</b>

A pointer to a string that contains the application display name. Memory for this string must be allocated using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -field pszVersion

Type: <b>LPWSTR</b>

Not applicable to published applications.

### -field pszPublisher

### -field pszProductID

Type: <b>LPWSTR</b>

Not applicable to published applications.

### -field pszRegisteredOwner

Type: <b>LPWSTR</b>

Not applicable to published applications.

### -field pszRegisteredCompany

Type: <b>LPWSTR</b>

Not applicable to published applications.

### -field pszLanguage

Type: <b>LPWSTR</b>

Not applicable to published applications.

Type: <b>LPWSTR</b>

Not applicable to published applications.

### -field pszSupportUrl

Type: <b>LPWSTR</b>

A URL to support information. This string is displayed as a link with the application name in Control Panel Add/Remove Programs. Memory for this string must be allocated using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -field pszSupportTelephone

Type: <b>LPWSTR</b>

Not applicable to published applications.

### -field pszHelpLink

Type: <b>LPWSTR</b>

Not applicable to published applications.

### -field pszInstallLocation

Type: <b>LPWSTR</b>

Not applicable to published applications.

### -field pszInstallSource

Type: <b>LPWSTR</b>

Not applicable to published applications.

### -field pszInstallDate

Type: <b>LPWSTR</b>

Not applicable to published applications.

### -field pszContact

Type: <b>LPWSTR</b>

Not applicable to published applications.

### -field pszComments

Type: <b>LPWSTR</b>

Not applicable to published applications.

### -field pszImage

Type: <b>LPWSTR</b>

Not applicable to published applications.

### -field pszReadmeUrl

Type: <b>LPWSTR</b>

Not applicable to published applications.

### -field pszUpdateInfoUrl

Type: <b>LPWSTR</b>

Not applicable to published applications.

## -see-also

<a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>



<a href="/windows/desktop/api/shappmgr/nf-shappmgr-ipublishedapp-getpublishedappinfo">IPublishedApp::GetPublishedAppInfo</a>