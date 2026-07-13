---
UID: NF:adshlp.ADsOpenObject
title: ADsOpenObject function (adshlp.h)
description: Binds to an ADSI object using explicit user name and password credentials.
helpviewer_keywords: ["ADsOpenObject","ADsOpenObject function [ADSI]","_ds_adsopenobject","adshlp/ADsOpenObject","adsi.adsopenobject"]
old-location: adsi\adsopenobject.htm
tech.root: adsi
ms.assetid: c4b85d8e-b33b-47a4-b7d7-5f901f80dce9
ms.date: 12/05/2018
ms.keywords: ADsOpenObject, ADsOpenObject function [ADSI], _ds_adsopenobject, adshlp/ADsOpenObject, adsi.adsopenobject
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
 - ADsOpenObject
 - adshlp/ADsOpenObject
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
 - ADsOpenObject
---

# ADsOpenObject function


## -description

The <b>ADsOpenObject</b> function binds to an ADSI object using explicit user name and password credentials.<b>ADsOpenObject</b> is a wrapper function for <a href="/windows/desktop/api/iads/nn-iads-iadsopendsobject">IADsOpenDSObject</a> and is equivalent to the <a href="/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject">IADsOpenDSObject::OpenDsObject</a> method.

## -parameters

### -param lpszPathName [in]

Type: <b>LPCWSTR</b>

The null-terminated Unicode string that specifies the ADsPath of the ADSI object. For more information and code examples of binding strings for this parameter, see  <a href="/windows/desktop/ADSI/ldap-adspath">LDAP ADsPath</a> and  <a href="/windows/desktop/ADSI/winnt-adspath">WinNT ADsPath</a>.

### -param lpszUserName [in]

Type: <b>LPCWSTR</b>

The null-terminated Unicode string that specifies the user name to supply to the directory service to use for credentials. This string should always be in the format "&lt;domain\\&gt;&lt;user name&gt;" to avoid ambiguity. For example, if DomainA and DomainB have a trust relationship and both domains have a user with the name "user1", it is not possible to predict which domain <b>ADsOpenObject</b> will use to validate "user1".

### -param lpszPassword [in]

Type: <b>LPCWSTR</b>

The null-terminated Unicode string that specifies the password to supply to the directory service to use for credentials.

### -param dwReserved [in]

Type: <b>DWORD</b>

Provider-specific authentication flags used to define the binding options. For more information, see  <a href="/windows/win32/api/iads/ne-iads-ads_authentication_enum">ADS_AUTHENTICATION_ENUM</a>.

### -param riid [in]

Type: <b>REFIID</b>

Interface identifier for the requested interface on this object.

### -param ppObject [out]

Type: <b>VOID**</b>

Pointer to a  pointer to the requested interface.

## -returns

Type: <b>HRESULT</b>

This method supports the standard <b>HRESULT</b> return values, including the following.

For more information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

This function should not be used just to validate user credentials.

A C/C++ client calls the <b>ADsOpenObject</b> helper function to bind to an ADSI object, using the user name and password supplied as credentials for the appropriate directory service. If <i>lpszUsername</i> and <i>lpszPassword</i> are <b>NULL</b> and <b>ADS_SECURE_AUTHENTICATION</b> is set, ADSI binds to the object using the security context of the calling thread, which is either the security context of the user account under which the application is running or of the client user account that the calling thread impersonates.

The  credentials passed to the <b>ADsOpenObject</b> function are used only with the particular object bound to and do not affect the security context of the calling thread. This means that, in the example below, the call to <b>ADsOpenObject</b> will use different credentials than the call to <a href="/windows/desktop/api/adshlp/nf-adshlp-adsgetobject">ADsGetObject</a>.


```cpp
HRESULT hr;
IADs *padsRoot1;
IADs *padsRoot2;

hr = ADsOpenObject(L"LDAP://rootDSE",
    pwszUsername,
    pwszPassword,
    ADS_SECURE_AUTHENTICATION,
    IID_IADs,
    (LPVOID*)&padsRoot1);

hr = ADsGetObject(L"LDAP://rootDSE",
    IID_IADs,
    (LPVOID*)&padsRoot2);

```


To work with the WinNT: provider, you can pass in <i>lpszUsername</i> as one of the following strings:

<ul>
<li>The name of a user account, that is, "jeffsmith".</li>
<li>The Windows style user name, that is, "Fabrikam\jeffsmith".</li>
</ul>
With the LDAP provider for Active Directory, you may pass in <i>lpszUsername</i> as one of the following strings:

<ul>
<li>The name of a user account, such as "jeffsmith". To use a user name by itself, you must set only the <b>ADS_SECURE_AUTHENTICATION</b> flag in the <i>dwReserved</i> parameter.</li>
<li>The user path from a previous version of Windows, such as "Fabrikam\jeffsmith".</li>
<li>Distinguished Name, such as "CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com". To use a DN, the <i>dwReserved</i> parameter must be zero or it must include the <b>ADS_USE_SSL</b> flag.</li>
<li>User Principal Name (UPN), such as "jeffsmith@Fabrikam.com". To use a UPN, assign the appropriate UPN value for the <b>userPrincipalName</b> attribute of the target user object.</li>
</ul>
If Kerberos authentication is required for the successful completion of a specific directory request using the LDAP provider, the <i>lpszPathName</i> binding string must use either a serverless ADsPath, such as "LDAP://CN=Jeff Smith,CN=admin,DC=Fabrikam,DC=com", or it must use an ADsPath with a fully qualified DNS server name, such as "LDAP://central3.corp.Fabrikam.com/CN=Jeff Smith,CN=admin,DC=Fabrikam,DC=com". Binding to the server using a flat NETBIOS name or a short DNS name, for example, using the short name "central3" instead of "central3.corp.Fabrikam.com", may or may not yield Kerberos authentication.

The following code example shows how to bind to a directory service object with the requested user credentials.


```cpp
IADs *pObject;
LPWSTR szUsername = NULL;
LPWSTR szPassword = NULL
HRESULT hr;

// Insert code to securely retrieve the user name and password.

hr = ADsOpenObject(L"LDAP://CN=Jeff,DC=Fabrikam,DC=com",
                   "jeffsmith",
                   "etercespot",
                   ADS_SECURE_AUTHENTICATION, 
                   IID_IADs,
                   (void**) &pObject);
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="/windows/desktop/ADSI/binding-with-adsopenobject-and-iadsopendsobject-opendsobject">ADsOpenObject and IADsOpenDSObject::OpenDsObject</a>



<a href="/windows/desktop/wsw/binding">Binding</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsopendsobject">IADsOpenDSObject</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject">IADsOpenDSObject::OpenDsObject</a>
