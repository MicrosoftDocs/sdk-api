---
UID: NF:iads.IADsServiceOperations.SetPassword
title: IADsServiceOperations::SetPassword
author: windows-sdk-content
description: The IADsServiceOperations::SetPassword method sets the password for the account used by the service manager. This method is called when the security context for this service is created.
old-location: adsi\iadsserviceoperations_setpassword.htm
tech.root: ADSI
ms.assetid: a10684d1-be61-4599-b232-638b416aa127
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IADsServiceOperations interface [ADSI],SetPassword method, IADsServiceOperations.SetPassword, IADsServiceOperations::SetPassword, SetPassword, SetPassword method [ADSI], SetPassword method [ADSI],IADsServiceOperations interface, _ds_iadsserviceoperations_setpassword, adsi.iadsserviceoperations__setpassword, adsi.iadsserviceoperations_setpassword, iads/IADsServiceOperations::SetPassword
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsServiceOperations.SetPassword
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsServiceOperations::SetPassword


## -description


The <b>IADsServiceOperations::SetPassword</b> method sets the password for the account used by the service manager. This method is called when the security context for this service is created.


## -parameters




### -param bstrNewPassword [in]

The null-terminated Unicode string to be stored as the new password.


## -returns



This method supports the standard return values, including S_OK. For more information about other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The property <a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">IADsService::get_ServiceAccountName</a> identifies the account for which this password is to be set.


#### Examples

The following code example shows how to set a password for the Microsoft Fax Service running on Windows 2000.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim cp As IADsComputer
Dim so As IADsServiceOperations
Dim s As IADsService
Dim sPass As String

On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
Set so = cp.GetObject("Service", "Fax")
' Insert code to securely retrieve a new password from the user.
so.SetPassword sPass
 
Set s = so
MsgBox "The password for " &amp; so.name &amp; " has been changed on "_
        &amp; s.ServiceAccountName

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set cp = Nothing
    Set so = Nothing
    Set s = Nothing
</pre>
</td>
</tr>
</table></span></div>
The following code example shows how to set a password for the Microsoft Fax Service running on Windows 2000.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT SetServicePassword(LPCWSTR pwszADsPath, LPCWSTR, pwszPasword)
{
    IADsContainer *pCont = NULL;
    IADsServiceOperations *pSrvOp = NULL;
    IDispatch *pDisp = NULL;
    HRESULT hr = S_OK;

    hr = ADsGetObject(pwszADsPath, IID_IADsContainer, (void**)&amp;pCont);
    if(FAILED(hr)) 
    {
        goto Cleanup;
    }

    hr = pCont-&gt;GetObject(CComBSTR("Service"), CComBSTR("Fax"), &amp;pDisp);
    if(FAILED(hr)) 
    {
        goto Cleanup;
    }

    hr = pDisp-&gt;QueryInterface(IID_IADsServiceOperations, (void**)&amp;pSrvOp);
    if(FAILED(hr)) 
    {
        goto Cleanup;
    }

    // Insert code to securely retrieve the password from the user.
    hr = pSrvOp-&gt;SetPassword(CComBSTR(pwszPassword));

Cleanup:
    if(pDisp) 
    {
        pDisp-&gt;Release();
    }
    if(pCont) 
    {
        pCont-&gt;Release();
    }
    if(pSrvOp) 
    {
        pSrvOp-&gt;Release();
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b59a6594-1109-4913-8a83-4888e56e71d0">IADsService</a>



<a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">IADsService::get_ServiceAccountName</a>



<a href="https://msdn.microsoft.com/f2459ca2-8a14-4343-bec6-ef3775dbf415">IADsServiceOperations</a>
 

 

