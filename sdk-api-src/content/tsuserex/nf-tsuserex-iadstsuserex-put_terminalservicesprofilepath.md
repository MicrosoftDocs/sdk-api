---
UID: NF:tsuserex.IADsTSUserEx.put_TerminalServicesProfilePath
title: IADsTSUserEx::put_TerminalServicesProfilePath (tsuserex.h)
description: The roaming or mandatory profile path to be used when the user logs on to the Remote Desktop Session Host (RD Session Host) server. (Put)
helpviewer_keywords: ["IADsTSUserEx interface [Remote Desktop Services]","TerminalServicesProfilePath property","IADsTSUserEx.TerminalServicesProfilePath","IADsTSUserEx.put_TerminalServicesProfilePath","IADsTSUserEx::TerminalServicesProfilePath","IADsTSUserEx::get_TerminalServicesProfilePath","IADsTSUserEx::put_TerminalServicesProfilePath","TerminalServicesProfilePath property [Remote Desktop Services]","TerminalServicesProfilePath property [Remote Desktop Services]","IADsTSUserEx interface","put_TerminalServicesProfilePath","termserv.iadstsuserex_terminalservicesprofilepath","tsuserex/IADsTSUserEx::TerminalServicesProfilePath","tsuserex/IADsTSUserEx::get_TerminalServicesProfilePath","tsuserex/IADsTSUserEx::put_TerminalServicesProfilePath"]
old-location: termserv\iadstsuserex_terminalservicesprofilepath.htm
tech.root: TermServ
ms.assetid: 282c20ab-378d-4205-90d3-6d28b0770adc
ms.date: 12/05/2018
ms.keywords: IADsTSUserEx interface [Remote Desktop Services],TerminalServicesProfilePath property, IADsTSUserEx.TerminalServicesProfilePath, IADsTSUserEx.put_TerminalServicesProfilePath, IADsTSUserEx::TerminalServicesProfilePath, IADsTSUserEx::get_TerminalServicesProfilePath, IADsTSUserEx::put_TerminalServicesProfilePath, TerminalServicesProfilePath property [Remote Desktop Services], TerminalServicesProfilePath property [Remote Desktop Services],IADsTSUserEx interface, put_TerminalServicesProfilePath, termserv.iadstsuserex_terminalservicesprofilepath, tsuserex/IADsTSUserEx::TerminalServicesProfilePath, tsuserex/IADsTSUserEx::get_TerminalServicesProfilePath, tsuserex/IADsTSUserEx::put_TerminalServicesProfilePath
req.header: tsuserex.h
req.include-header: Tsuserex.h, Tsuserex_i.c
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
req.type-library: Tsuserex.tlb
req.lib: 
req.dll: Tsuserex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsTSUserEx::put_TerminalServicesProfilePath
 - tsuserex/IADsTSUserEx::put_TerminalServicesProfilePath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tsuserex.dll
api_name:
 - IADsTSUserEx.TerminalServicesProfilePath
 - IADsTSUserEx.get_TerminalServicesProfilePath
 - IADsTSUserEx.put_TerminalServicesProfilePath
---

# IADsTSUserEx::put_TerminalServicesProfilePath


## -description

The roaming or mandatory profile path to be used when the user logs on to the Remote Desktop Session Host (RD Session Host) server.

This property is read/write.

## -parameters

## -remarks

The profile path is 
     in the following network path format:

<b>\\\\</b><i>ServerName</i><b>\\</b><i>ProfilesFolderName</i><b>\\</b><i>UserName</i>

<div class="alert"><b>Note</b>  A Remote Desktop Services profile path is used only for logging on to an RD Session Host server.</div>
<div> </div>

#### Examples

The following example shows a program that binds to the Active Directory database without credentials.


```cpp
 IADsContainer *pContainer = NULL;
 IDispatch *pNewObject = NULL;
 IADsTSUserEx *pTSUser = NULL;
 IADsUser *pUser = NULL;
 HRESULT hr = ERROR_SUCCESS;

 CoInitialize(NULL);
 //
 // Bind to the known container.
 //
 hr = ADsGetObject(
    L"LDAP://DOMAIN/CN=Users,DC=Server1,DC=Domain,DC=com",
    IID_IADsContainer,
    (void**)&pContainer);

 if( !SUCCEEDED(hr)) {
  wprintf(L"ADsGetObject ret failed with 0x%x\n", hr);
  return FALSE;
 }
 //
 // Create the new Active Directory Service Interfaces User object.
 //
 hr = pContainer->Create(L"user",
                         L"cn=test3",
                         &pNewObject);
 pContainer->Release();

 if( !SUCCEEDED(hr)) {
  wprintf(L"Create ret failed with 0x%x\n", hr);
  return FALSE;
 }
 //
 // Get the IADsTSUser interface from the user object.
 //
 hr = pNewObject->QueryInterface(IID_IADsTSUserEx, (void**)&pTSUser);

 if( !SUCCEEDED(hr)) { 
  wprintf(L"QueryInterface for IADsTSUserEx failed with ret 0x%x\n",
          hr);
  return FALSE;
 }
 //
 // Get the IADsTSUser interface from the user object.
 //
 hr = pNewObject->QueryInterface(IID_IADsUser, (void**)&pUser);

 if( !SUCCEEDED(hr)) {
  wprintf(L"QueryInterface for IAsUser failed with 0x%x\n", hr);
  return FALSE;
 }
 pNewObject->Release();

 //
 // Set TerminalServicesProfilePath
 //
 pTSUser->put_TerminalServicesProfilePath(L"c:\\windows");
 pTSUser->Release();

 //
 // Commit the object data to the directory.
 //
 pUser->SetInfo();
 pUser->Release();
 CoUninitialize();

```


You can use the following script examples to bind to a provider's namespace. Two examples bind with supplied 
     credentials; two bind without credentials.

The first example shows a script that binds to the Security Accounts Manager (SAM) database with the 
      supplied credentials.

The second example shows a script that binds to the Active Directory database with the supplied 
     credentials.


```vb
Set DSO = GetObject("WinNT:")
Set usr = DSO.OpenDSObject(
    "WinNT://Server1/Test,user",
    Domain\User,
    Password,
    ADS_SECURE_AUTHENTICATION)
Wscript.echo usr.TerminalServicesProfilePath
usr.TerminalServicesProfilePath = "profile path"
usr.SetInfo
WScript.echo usr.TerminalServicesProfilePath

```

```vb
Set DSO = GetObject("LDAP:")
Set usr = DSO.OpenDSObject(
    "LDAP://DOMAIN/CN=Test,CN=Users,DC=Server1,DC=Domain,DC=com",
    Domain\User,
    Password,
    ADS_SECURE_AUTHENTICATION)
Wscript.echo usr.TerminalServicesProfilePath
usr.TerminalServicesProfilePath = "profile path"
usr.SetInfo
WScript.echo usr.TerminalServicesProfilePath

```

## -see-also

<a href="/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex">IADsTSUserEx</a>
