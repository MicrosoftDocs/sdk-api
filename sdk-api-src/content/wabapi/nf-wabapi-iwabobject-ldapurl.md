---
UID: NF:wabapi.IWABObject.LDAPUrl
title: IWABObject::LDAPUrl (wabapi.h)
description: Processes an Lightweight Directory Access Protocol (LDAP) URL and displays the results obtained from the URL.
helpviewer_keywords: ["IWABObject interface [Windows Address Book]","LDAPUrl method","IWABObject.LDAPUrl","IWABObject::LDAPUrl","LDAPUrl","LDAPUrl method [Windows Address Book]","LDAPUrl method [Windows Address Book]","IWABObject interface","LDAP_AUTH_NEGOTIATE","MAPI_UNICODE","WABOBJECT_LDAPURL_RETURN_MAILUSER","_wab_IWABObject_LDAPUrl","wab._wab_IWABObject_LDAPUrl","wabapi/IWABObject::LDAPUrl"]
old-location: wab\_wab_IWABObject_LDAPUrl.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\ldapurl.htm
ms.date: 12/05/2018
ms.keywords: IWABObject interface [Windows Address Book],LDAPUrl method, IWABObject.LDAPUrl, IWABObject::LDAPUrl, LDAPUrl, LDAPUrl method [Windows Address Book], LDAPUrl method [Windows Address Book],IWABObject interface, LDAP_AUTH_NEGOTIATE, MAPI_UNICODE, WABOBJECT_LDAPURL_RETURN_MAILUSER, _wab_IWABObject_LDAPUrl, wab._wab_IWABObject_LDAPUrl, wabapi/IWABObject::LDAPUrl
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IWABObject::LDAPUrl
 - wabapi/IWABObject::LDAPUrl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IWABObject.LDAPUrl
---

# IWABObject::LDAPUrl


## -description

Processes an Lightweight Directory Access Protocol (LDAP) URL 
		and displays the results obtained from the URL. 
		If the URL only contains a server name, 
		the Windows Address Book (WAB) launches the Find window with the server name 
		filled in. If the URL contains an 
		LDAP query, the query is processed. If the query has 
		a single result, the WAB shows details about the result; 
		if the query has multiple results, the WAB shows the Find 
		dialog box with multiple search results filled in.

## -parameters

### -param lpIAB

Type: <b><a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a>*</b>

Pointer to an <a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a> interface 
				that specifies the address book to use.

### -param hWnd

Type: <b>HWND</b>

Value of type <b>HWND</b> that specifies the 
				handle to the parent window for displayed dialog boxes.

### -param ulFlags

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies flags 
				that affect functionality.



#### WABOBJECT_LDAPURL_RETURN_MAILUSER

Indicates that a Mailuser object is to be returned if 
				the query returns a single result. If the query returns multiple
				 hits, the WAB returns MAPI_E_AMBIGUOUS_RECIPIENT.
				 



#### LDAP_AUTH_NEGOTIATE

Indicates that the WAB must attempt a 
				negotiated bind with the server.



#### MAPI_UNICODE

Indicates that <i>lpszURL</i> must be cast to a
				<b>LPWSTR</b> before using it.

### -param lpszURL

Type: <b>LPSTR</b>

Value of type <b>LPSTR</b> that specifies the 
				LDAP URL string. This 
				string must begin with "ldap://".

### -param lppMailUser

Type: <b><a href="/windows/desktop/api/wabdefs/nn-wabdefs-imailuser">IMailUser</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/wabdefs/nn-wabdefs-imailuser">IMailUser</a> 
				interface that receives the returned Mailuser object, 
				if requested. Otherwise, it is <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default behavior for this API is to bind anonymously to the 
	LDAP server. To specify a negotiated bind, you can pass 
	<b>LDAP_AUTH_NEGOTIATE</b> into <i>ulFlags</i>. 
	This flag is defined in Winldap.h.

To pass in a Unicode LDAP 
				URL without losing any data, cast the 
	URL pointer to a <b>LPSTR</b> and pass it into 
	this function. Mark <i>ulFlags</i> to include <b>MAPI_UNICODE</b>, and the WAB will cast the 
	URL back to an <b>LPWSTR</b> prior to using it.