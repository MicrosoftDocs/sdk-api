---
UID: NF:iads.IADsOpenDSObject.OpenDSObject
title: IADsOpenDSObject::OpenDSObject (iads.h)
description: Binds to an ADSI object, using the given credentials, and retrieves an IDispatch pointer to the specified object.
helpviewer_keywords: ["IADsOpenDSObject interface [ADSI]","OpenDSObject method","IADsOpenDSObject.OpenDSObject","IADsOpenDSObject::OpenDSObject","OpenDSObject","OpenDSObject method [ADSI]","OpenDSObject method [ADSI]","IADsOpenDSObject interface","_ds_iadsopendsobject_opendsobject","adsi.iadsopendsobject__opendsobject","adsi.iadsopendsobject_opendsobject","iads/IADsOpenDSObject::OpenDSObject"]
old-location: adsi\iadsopendsobject_opendsobject.htm
tech.root: adsi
ms.assetid: 9984ddb4-58bb-4264-930b-07e6534dc69f
ms.date: 12/05/2018
ms.keywords: IADsOpenDSObject interface [ADSI],OpenDSObject method, IADsOpenDSObject.OpenDSObject, IADsOpenDSObject::OpenDSObject, OpenDSObject, OpenDSObject method [ADSI], OpenDSObject method [ADSI],IADsOpenDSObject interface, _ds_iadsopendsobject_opendsobject, adsi.iadsopendsobject__opendsobject, adsi.iadsopendsobject_opendsobject, iads/IADsOpenDSObject::OpenDSObject
req.header: iads.h
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsOpenDSObject::OpenDSObject
 - iads/IADsOpenDSObject::OpenDSObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsOpenDSObject.OpenDSObject
---

# IADsOpenDSObject::OpenDSObject

## -description

The <b>IADsOpenDSObject::OpenDSObject</b> method binds to an ADSI object, using the given credentials, and retrieves an  <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> pointer to the specified object.
<div class="alert"><b>Important</b>  It is not recommended that you use this method with the WinNT Provider. For more information, please see KB article 218497, <a href="/troubleshoot/windows-client/admin-development/adsi-winnt-provider-user-authentication-issues">User authentication issues with the Active Directory Service Interfaces WinNT provider</a>.</div><div> </div>

## -parameters

### -param lpszDNName [in]

The null-terminated Unicode string that specifies the ADsPath of the ADSI object. For more information and examples of binding strings for this parameter, see  <a href="/windows/desktop/ADSI/ldap-adspath">LDAP ADsPath</a>. When using the LDAP provider with an ADsPath that includes a specific server name, the <i>lnReserved</i> parameter should include the <b>ADS_SERVER_BIND</b> flag.

### -param lpszUserName [in]

The null-terminated Unicode string that specifies the user name to be used for securing permission from the namespace server. For more information, see the following Remarks section.

### -param lpszPassword [in]

The null-terminated Unicode string that specifies the password to be used to obtain permission from the namespace server.

### -param lnReserved [in]

Authentication flags used to define the binding options. For more information, see  <a href="/windows/win32/api/iads/ne-iads-ads_authentication_enum">ADS_AUTHENTICATION_ENUM</a>.

### -param ppOleDsObj [out]

Pointer to a pointer to an  <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface on the requested object.

## -returns

This method supports the standard return values, including <b>S_OK</b> when the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface has been successfully retrieved using these credentials.
      

For more information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

This method should not be used just to validate user credentials. 

When <i>lnReserved</i> is set, the behavior of <b>OpenDSObject</b> depends on the provider it connects to. High security namespaces may ignore these flags and always require authentication.

The <b>IADsOpenDSObject::OpenDSObject</b> method maintains the authenticated and encrypted user credentials in the cache. Cached credentials may be used in subsequent operations for binding to any other directory objects. The ADSI client applications should not cache the credentials supplied by the user. Instead, they should rely on ADSI infrastructure to perform  caching. To use the cached credentials, <i>lpszPassword</i> and <i>lpszUserName</i> must remain unchanged in any subsequent calls of <b>OpenDSObject</b>. The following code example shows this operation.


```vb
Dim dso As IADsOpenDSObject
Dim obj1, obj2 As IADs
Dim szUsername As String
Dim szPassword As String

Set dso = GetObject("LDAP:")

' Insert code securely.

' Supply full credentials to initiate a server connection.
Set obj1 = dso.OpenDSObject( _
    "LDAP://server1/CN=Dept1,DC=Fabrikam,DC=com", _
    szUsername, _
    szPassword, _
    ADS_SECURE_AUTHENTICATION + ADS_SERVER_BIND)

' Perform an operation with the bound object, obj1
MsgBox obj1.Class

' Bind to another object with the cached user credential.
Set obj2 = dso.OpenDSObject( _
    "LDAP://server1/CN=Dept2,DC=Fabrikam,DC=com", _
    szUsername, _
    szPassword, _
    ADS_SECURE_AUTHENTICATION + ADS_SERVER_BIND)

MsgBox obj2.Class

```


The  credentials passed to the <b>IADsOpenDSObject::OpenDSObject</b> function are used only with the particular object bound to and do not affect the security context of the calling thread. This means that, in the following code example, the  call to <b>IADsOpenDSObject::OpenDSObject</b> will use different credentials than the  call to <b>GetObject</b>.


```vb
Dim dso As IADsOpenDSObject
Dim obj1, obj2 As IADs
Dim szUsername As String
Dim szPassword As String

Set dso = GetObject("LDAP:")

' Insert code securely.

' Bind using full credentials.
Set obj1 = dso.OpenDSObject( _
    "LDAP://server1/CN=Dept1,DC=Fabrikam,DC=com", _
    szUsername, _
    szPassword, _
    ADS_SECURE_AUTHENTICATION + ADS_SERVER_BIND)

' Bind to another object with the default credentials.
Set obj2 = GetObject("LDAP://server1/CN=Dept2,DC=Fabrikam,DC=com")
```


With a serverless binding, the server name, "server1", is not stated explicitly. The default server is used instead. Only the LDAP provider supports the serverless binding. To use this feature, the client computer must be on an Active Directory domain. To attempt a serverless binding from a computer, you must bind as a domain user.

For credential caching to work properly, it is important to keep an object reference outstanding to maintain the cache handle. In the example given above, an attempt to open "obj2" after releasing "obj1" will result in an authentication failure.

The <a href="/windows/desktop/api/iads/nn-iads-iadsopendsobject">IADsOpenDSObject</a> method uses the default credentials when <i>lpszUserName</i> and <i>lpszPassword</i> are set to <b>NULL</b>.

If Kerberos authentication is required for the successful completion of a specific directory request using the LDAP provider, the <i>lpszDNName</i> binding string must use either a serverless ADsPath, such as "LDAP://CN=Jeff Smith,CN=admin,DC=Fabrikam,DC=com", or it must use an ADsPath with a fully qualified DNS server name, such as "LDAP://central3.corp.Fabrikam.com/CN=Jeff Smith,CN=admin,DC=Fabrikam,DC=com". Binding to the server using a flat NETBIOS name or a short DNS name, for example, using the short name "central3" instead of "central3.corp.Fabrikam.com", may or may not yield Kerberos authentication.

The  <a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a> helper function offers the same features as the <b>IADsOpenDSObject::OpenDSObject</b> method.

With the LDAP provider for Active Directory, you may pass in <i>lpszUserName</i> as one of the following strings:

<ul>
<li>The name of a user account, such as "jeffsmith". To use a user name by itself, you must set only the <b>ADS_SECURE_AUTHENTICATION</b> flag in the <i>lnReserved</i> parameter.</li>
<li>The user path from a previous version of Windows, such as "Fabrikam\jeffsmith".</li>
<li>Distinguished Name, such as "CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com". To use a DN, the <i>lnReserved</i> parameter must be zero or it must include the <b>ADS_USE_SSL</b> flag</li>
<li>User Principal Name (UPN), such as "jeffsmith@Fabrikam.com". To use a UPN, you must assign the appropriate UPN value for the <i>userPrincipalName</i> attribute of the target user object.</li>
</ul>

#### Examples

The following code example shows how to use <a href="/windows/desktop/api/iads/nn-iads-iadsopendsobject">IADsOpenDSObject</a> to open the "Administrator" user object on "Fabrikam" with Secure Authentication through the LDAP provider.


```vb
Dim dso As IADsOpenDSObject
Dim domain As IADsDomain
Dim szUsername As String
Dim szPassword As String

On Error GoTo Cleanup

' Insert code to securely retrieve the user name and password.
 
Set dso = GetObject("LDAP:")
Set domain = dso.OpenDSObject("LDAP://Fabrikam", szUsername, _
                              szPassword, _
                              ADS_SECURE_AUTHENTICATION)

Cleanup:
    If (Err.Number <> 0 ) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set dso = Nothing
    Set domain = Nothing
```


The following code example uses <a href="/windows/desktop/api/iads/nn-iads-iadsopendsobject">IADsOpenDSObject</a> to open an Active Directory object through the LDAP provider.


```cpp
IADsOpenDSObject *pDSO = NULL;
HRESULT hr = S_OK;
 
hr = ADsGetObject(L"LDAP:", IID_IADsOpenDSObject, (void**) &pDSO);
if (SUCCEEDED(hr))
{
    IDispatch *pDisp;
    hr = pDSO->OpenDSObject(CComBSTR("LDAP://DC=Fabrikam, DC=com"), 
                       CComBSTR("jeffsmith@Fabrikam.com"),
                       CComBSTR("passwordhere"),
                       ADS_SECURE_AUTHENTICATION, 
                       &pDisp);
    pDSO->Release();
    if (SUCCEEDED(hr))
    {
        IADs *pADs;
        hr = pDisp->QueryInterface(IID_IADs, (void**) &pADs);
        pDisp->Release();
        if (SUCCEEDED(hr))
        {
        // Perform an object manipulation here.
            pADs->Release();
        }
    }
}
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error
  Codes</a>



<a href="/windows/win32/api/iads/ne-iads-ads_authentication_enum">ADS_AUTHENTICATION_ENUM</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a>



<a href="/windows/desktop/wsw/binding">Binding</a>



<a href="/windows/desktop/ADSI/binding-with-getobject-and-adsgetobject">GetObject</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsopendsobject">IADsOpenDSObject</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/ADSI/ldap-adspath">LDAP ADsPath</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a">WNetAddConnetion2</a>