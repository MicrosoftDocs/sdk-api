---
UID: NF:iads.IADsContainer.MoveHere
title: IADsContainer::MoveHere (iads.h)
description: Moves a specified object to the container that implements this interface.
helpviewer_keywords: ["IADsContainer interface [ADSI]","MoveHere method","IADsContainer.MoveHere","IADsContainer::MoveHere","MoveHere","MoveHere method [ADSI]","MoveHere method [ADSI]","IADsContainer interface","_ds_iadscontainer_movehere","adsi.iadscontainer__movehere","adsi.iadscontainer_movehere","iads/IADsContainer::MoveHere"]
old-location: adsi\iadscontainer_movehere.htm
tech.root: adsi
ms.assetid: 132b1cdc-6fb5-43b1-a5de-3b25c361e8e1
ms.date: 12/05/2018
ms.keywords: IADsContainer interface [ADSI],MoveHere method, IADsContainer.MoveHere, IADsContainer::MoveHere, MoveHere, MoveHere method [ADSI], MoveHere method [ADSI],IADsContainer interface, _ds_iadscontainer_movehere, adsi.iadscontainer__movehere, adsi.iadscontainer_movehere, iads/IADsContainer::MoveHere
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
 - IADsContainer::MoveHere
 - iads/IADsContainer::MoveHere
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
 - IADsContainer.MoveHere
---

# IADsContainer::MoveHere


## -description

The <b>IADsContainer::MoveHere</b> method moves a specified object to the container that implements this interface.The method can be used to rename an object.

## -parameters

### -param SourceName [in]

The null-terminated Unicode string that specifies the <b>ADsPath</b> of the object to be moved.

### -param NewName [in]

The null-terminated Unicode string that specifies the relative name of the new object within the container. This can be
    <b>NULL</b>, in which case the object is moved. If it is not <b>NULL</b>, the object is
    renamed accordingly in the process.

### -param ppObject [out]

Pointer to a pointer to the 
     <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface on the moved
    object.

## -returns

This method supports standard return values, including
    <b>S_OK</b>, for a successful operation. For more information about error codes, see 
     <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

In Active Directory, you can move an object within the same domain
    or from different domains in the same directory forest. For the cross domain
    move, the following restrictions apply:

<ul>
<li>The destination domain must be in the native mode.</li>
<li>Objects to be moved must be a leaf object or an empty
    container.</li>
<li>NT LAN Manager (NTLM) cannot perform authentication; use Kerberos authentication or delegation. Be aware that if Kerberos authentication is not used, the password transmits in plaintext over the network. To avoid this, use delegation with secure authentication.</li>
<li>You cannot move security principals (for example, user, group, computer, and
    so on) belonging to a global group. When a security principal is moved, a new
    SID is created for the object at the destination. However, its old SID from the
    source, stored in the <b>sIDHistory</b> attribute,
    is preserved, as well as the password of the object.</li>
</ul>
<div class="alert"><b>Note</b>  Use the Movetree.exe utility to move a subtree among
    different domains. To move objects from a source domain to a destination domain
    using the Movetree command-line tool, you must connect to the domain controller
    holding the source domain's RID master role. If the RID master is unavailable
    then objects cannot be moved to other domains. If you attempt to move an object
    from one domain to another using the Movetree.exe tool and you specify a source
    domain controller that is not the RID master, a nonspecific "Movetree failed"
    error message results.</div>
<div> </div>
<div class="alert"><b>Note</b>  When using the 
     <a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a> function to bind to
    an ADSI object, you must use the <b>ADS_USE_DELEGATION</b> flag of the 
     <a href="/windows/win32/api/iads/ne-iads-ads_authentication_enum">ADS_AUTHENTICATION_ENUM</a> in the <i>dwReserved</i> parameter of this function
    in order to create cross-domain moves with <b>IADsContainer::MoveHere</b>. The
    <b>ADsOpenObject</b> function is equivalent to the 
     <a href="/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject">IADsOpenDSObject::OpenDsObject</a> method. Likewise, using the <b>OpenDsObject</b> method to bind to an ADSI object, the <i>InReserved</i> parameter of this method must contain the
    <b>ADS_USE_DELEGATION</b> flag of the
    <b>ADS_AUTHENTICATION_ENUM</b> in order to make cross-domain moves with
    <b>IADsContainer::MoveHere</b>.</div>
<div> </div>
The following code example moves the user, "jeffsmith" from the
    "South.Fabrikam.Com" domain to the "North.Fabrikam.Com" domain. First, it gets
    an <a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a> pointer to the destination
    container, then the <b>MoveHere</b> call specifies
    the path of the object to move.


```vb
Set ou = GetObject("LDAP://server1/OU=Support,DC=North,DC=Fabrikam,DC=COM")
ou.MoveHere("LDAP://server2/CN=jeffsmith,OU=Sales,DC=South,DC=Fabrikam,DC=Com", vbNullString)
```


A serverless ADsPath can be used for either the source or the
    destination or both.

The <b>IADsContainer::MoveHere</b> method can be used either to rename an object within the same container or to
    move an object among different containers. Moving an object retains the
    object RDN, whereas renaming an object alters the RDN.

For example, the following code example performs the rename action.


```vb
set cont = GetObject("LDAP://dc=dom,dc=com")
set newobj = cont.MoveHere("LDAP://cn=Jeff Smith,dc=dom,dc=com", "cn=Denise Smith")
```


The following code example performs the move.


```vb
set cont = GetObject("LDAP://dc=dom,dc=com")
set newobj = cont.MoveHere("LDAP://cn=jeffsmith,ou=sales,dc=dom,dc=com", "cn=jeffsmith")
```


In Visual Basic applications, you can pass
    <b>vbNullString</b> as the second parameter when
    moving an object from one container to another.


```vb
Set newobj =  cont.MoveHere("LDAP://cn=jeffsmith,ou=sale,dc=dom,dc=com", vbNullString)
```


However, you cannot do the same with VBScript. This is because
    VBScript maps <b>vbNullString</b> to an empty string instead of to a null string, as
    does Visual Basic. You must use the RDN explicitly, as shown in the previous
    example.

<div class="alert"><b>Note</b>  The WinNT provider supports <b>IADsContainer::MoveHere</b>, but only for renaming users &amp;
    groups within a domain.</div>
<div> </div>

#### Examples

The following code example shows how to use this method to rename
    an object.


```vb
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
' Rename an object.
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam,DC=com")
Set usr = cont.MoveHere("LDAP://CN=jeffsmith,OU=Sales, DC=Fabrikam,DC=com", "CN=jayhenningsen")
 
' Move an object.
cont.MoveHere("LDAP://CN=denisesmith,OU=Engineer,DC=Fabrikam,DC=com", vbNullString)

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing

```


The following code example moves a user object using the
    <b>IADsContainer::MoveHere</b> method.


```cpp
/////////////////////////////////////////////
// First, bind to the destination container.
////////////////////////////////////////////
HRESULT hr;
IADsContainer *pCont=NULL;
CoInitialize(NULL);
hr = ADsGetObject(
        L"LDAP://OU=MCS,DC=windows2000,DC=mytest,DC=fabrikam,DC=com",
        IID_IADsContainer,
        (void**) &pCont );
 
if ( !SUCCEEDED(hr) )
{
    goto Cleanup;
}
 
//////////////////////////////////////////////////
// Second, move the object to the bound container.
//////////////////////////////////////////////////
IDispatch *pDisp=NULL;
 
hr = pCont->MoveHere(CComBSTR("LDAP://CN=Jeff Smith,OU=DSys,DC=windows2000,DC=mytest,DC=fabrikam,DC=com"), NULL, &pDisp );
pCont->Release();
 
if (SUCCEEDED(hr) )
{ 
// You can perform another operation here, such as updating attributes.
pDisp->Release();
}

Cleanup:
    if(pCont)
        pCont->Release(); 

    if(pDisp)
        pDisp->Release();

    CoUninitialize();
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error
  Codes</a>



<a href="/windows/win32/api/iads/ne-iads-ads_authentication_enum">ADS_AUTHENTICATION_ENUM</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere">IADsContainer::CopyHere</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject">IADsOpenDSObject::OpenDsObject</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>