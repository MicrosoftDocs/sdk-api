---
UID: NF:iads.IADsServiceOperations.SetPassword
title: IADsServiceOperations::SetPassword (iads.h)
description: The IADsServiceOperations::SetPassword method sets the password for the account used by the service manager. This method is called when the security context for this service is created.
helpviewer_keywords: ["IADsServiceOperations interface [ADSI]","SetPassword method","IADsServiceOperations.SetPassword","IADsServiceOperations::SetPassword","SetPassword","SetPassword method [ADSI]","SetPassword method [ADSI]","IADsServiceOperations interface","_ds_iadsserviceoperations_setpassword","adsi.iadsserviceoperations__setpassword","adsi.iadsserviceoperations_setpassword","iads/IADsServiceOperations::SetPassword"]
old-location: adsi\iadsserviceoperations_setpassword.htm
tech.root: adsi
ms.assetid: a10684d1-be61-4599-b232-638b416aa127
ms.date: 12/05/2018
ms.keywords: IADsServiceOperations interface [ADSI],SetPassword method, IADsServiceOperations.SetPassword, IADsServiceOperations::SetPassword, SetPassword, SetPassword method [ADSI], SetPassword method [ADSI],IADsServiceOperations interface, _ds_iadsserviceoperations_setpassword, adsi.iadsserviceoperations__setpassword, adsi.iadsserviceoperations_setpassword, iads/IADsServiceOperations::SetPassword
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
 - IADsServiceOperations::SetPassword
 - iads/IADsServiceOperations::SetPassword
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
 - IADsServiceOperations.SetPassword
---

# IADsServiceOperations::SetPassword


## -description

The <b>IADsServiceOperations::SetPassword</b> method sets the password for the account used by the service manager. This method is called when the security context for this service is created.

## -parameters

### -param bstrNewPassword [in]

The null-terminated Unicode string to be stored as the new password.

## -returns

This method supports the standard return values, including S_OK. For more information about other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The property <a href="/windows/desktop/ADSI/iadsservice-property-methods">IADsService::get_ServiceAccountName</a> identifies the account for which this password is to be set.


#### Examples

The following code example shows how to set a password for the Microsoft Fax Service running on Windows 2000.


```vb
Dim cp As IADsComputer
Dim so As IADsServiceOperations
Dim s As IADsService
Dim sPass As String

On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
Set so = cp.GetObject("Service", "Fax")
' Insert code to securely retrieve a new password from the user.
so.SetPassword sPass
 
Set s = so
MsgBox "The password for " & so.name & " has been changed on "_
        & s.ServiceAccountName

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
    Set so = Nothing
    Set s = Nothing

```


The following code example shows how to set a password for the Microsoft Fax Service running on Windows 2000.


```cpp
HRESULT SetServicePassword(LPCWSTR pwszADsPath, LPCWSTR, pwszPasword)
{
    IADsContainer *pCont = NULL;
    IADsServiceOperations *pSrvOp = NULL;
    IDispatch *pDisp = NULL;
    HRESULT hr = S_OK;

    hr = ADsGetObject(pwszADsPath, IID_IADsContainer, (void**)&pCont);
    if(FAILED(hr)) 
    {
        goto Cleanup;
    }

    hr = pCont->GetObject(CComBSTR("Service"), CComBSTR("Fax"), &pDisp);
    if(FAILED(hr)) 
    {
        goto Cleanup;
    }

    hr = pDisp->QueryInterface(IID_IADsServiceOperations, (void**)&pSrvOp);
    if(FAILED(hr)) 
    {
        goto Cleanup;
    }

    // Insert code to securely retrieve the password from the user.
    hr = pSrvOp->SetPassword(CComBSTR(pwszPassword));

Cleanup:
    if(pDisp) 
    {
        pDisp->Release();
    }
    if(pCont) 
    {
        pCont->Release();
    }
    if(pSrvOp) 
    {
        pSrvOp->Release();
    }
}
```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iadsservice">IADsService</a>



<a href="/windows/desktop/ADSI/iadsservice-property-methods">IADsService::get_ServiceAccountName</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a>