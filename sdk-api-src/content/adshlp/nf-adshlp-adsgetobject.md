---
UID: NF:adshlp.ADsGetObject
title: ADsGetObject function (adshlp.h)
description: Binds to an object given its path and a specified interface identifier.
helpviewer_keywords: ["ADsGetObject","ADsGetObject function [ADSI]","_ds_adsgetobject","adshlp/ADsGetObject","adsi.adsgetobject"]
old-location: adsi\adsgetobject.htm
tech.root: adsi
ms.assetid: 595b2c7f-584c-4343-a75c-327d8ed4ceb1
ms.date: 12/05/2018
ms.keywords: ADsGetObject, ADsGetObject function [ADSI], _ds_adsgetobject, adshlp/ADsGetObject, adsi.adsgetobject
req.header: adshlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Activeds.lib
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ADsGetObject
 - adshlp/ADsGetObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-adsi-activeds-l1-1-0.dll
 - Activeds.dll
api_name:
 - ADsGetObject
---

# ADsGetObject function


## -description

The <b>ADsGetObject</b> function binds to an object given its path and a specified interface identifier.

## -parameters

### -param lpszPathName [in]

Type: <b>LPCWSTR</b>

The null-terminated Unicode string that specifies the path  used to bind to the object in the underlying directory service. For more information and code examples for binding strings for this parameter, see  <a href="/windows/desktop/ADSI/ldap-adspath">LDAP ADsPath</a> and  <a href="/windows/desktop/ADSI/winnt-adspath">WinNT ADsPath</a>.

### -param riid [in]

Type: <b>REFIID</b>

Interface identifier for a specified interface on this object.

### -param ppObject [out]

Type: <b>VOID**</b>

Pointer to a pointer to the requested Interface.

## -returns

Type: <b>HRESULT</b>

This method supports the standard <b>HRESULT</b> return values, as well as the following.

For more information about other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

A C/C++ client calls the <b>ADsGetObject</b> helper function to bind to an ADSI object. It is equivalent to a Visual Basic client calling the <a href="/windows/desktop/ADSI/binding-with-getobject-and-adsgetobject">GetObject</a> function. They both take an ADsPath as input and returns a pointer to the requested interface. By default the binding uses ADS_SECURE_AUTHENTICATION option with the security context of the calling thread. However, if the authentication fails, the secure bind is downgraded to an anonymous bind, for example, a simple bind without user credentials. To securely bind to an ADSI object, use the <a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a> function instead of the  <b>ADsGetObject</b> function.

For a code example that shows how to use <a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a>, see <a href="/windows/desktop/ADSI/binding-with-getobject-and-adsgetobject">Binding With GetObject and ADsGetObject</a>.

It is possible to bind to an ADSI object with a user credential different from that of the currently logged-on user. To perform this operation, use the   <a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a> function.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a>



<a href="/windows/desktop/ADSI/binding-with-getobject-and-adsgetobject">Binding With GetObject and ADsGetObject</a>