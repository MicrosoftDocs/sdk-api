---
UID: NF:tsuserex.IADsTSUserEx.put_TerminalServicesProfilePath
title: IADsTSUserEx::put_TerminalServicesProfilePath
author: windows-driver-content
description: The roaming or mandatory profile path to be used when the user logs on to the Remote Desktop Session Host (RD Session Host) server.
old-location: termserv\iadstsuserex_terminalservicesprofilepath.htm
old-project: TermServ
ms.assetid: 282c20ab-378d-4205-90d3-6d28b0770adc
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IADsTSUserEx interface [Remote Desktop Services],TerminalServicesProfilePath property, IADsTSUserEx.TerminalServicesProfilePath, IADsTSUserEx.put_TerminalServicesProfilePath, IADsTSUserEx::TerminalServicesProfilePath, IADsTSUserEx::get_TerminalServicesProfilePath, IADsTSUserEx::put_TerminalServicesProfilePath, TerminalServicesProfilePath property [Remote Desktop Services], TerminalServicesProfilePath property [Remote Desktop Services],IADsTSUserEx interface, put_TerminalServicesProfilePath, termserv.iadstsuserex_terminalservicesprofilepath, tsuserex/IADsTSUserEx::TerminalServicesProfilePath, tsuserex/IADsTSUserEx::get_TerminalServicesProfilePath, tsuserex/IADsTSUserEx::put_TerminalServicesProfilePath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WTSSBX_SESSION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tsuserex.dll
api_name:
-	IADsTSUserEx.TerminalServicesProfilePath
-	IADsTSUserEx.get_TerminalServicesProfilePath
-	IADsTSUserEx.put_TerminalServicesProfilePath
product: Windows
targetos: Windows
req.lib: 
req.dll: Tsuserex.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IADsTSUserEx::put_TerminalServicesProfilePath


## -description


The roaming or mandatory profile path to be used when the user logs on to the Remote Desktop Session Host (RD Session Host) server.

This property is read/write.


## -parameters


## -remarks



The profile path is 
     in the following network path format:

<b>\\</b><i>ServerName</i><b>\</b><i>ProfilesFolderName</i><b>\</b><i>UserName</i>

<div class="alert"><b>Note</b>  A Remote Desktop Services profile path is used only for logging on to an RD Session Host server.</div>
<div> </div>

#### Examples

The following example shows a program that binds to the Active Directory database without credentials.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre> IADsContainer *pContainer = NULL;
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
    (void**)&amp;pContainer);

 if( !SUCCEEDED(hr)) {
  wprintf(L"ADsGetObject ret failed with 0x%x\n", hr);
  return FALSE;
 }
 //
 // Create the new Active Directory Service Interfaces User object.
 //
 hr = pContainer-&gt;Create(L"user",
                         L"cn=test3",
                         &amp;pNewObject);
 pContainer-&gt;Release();

 if( !SUCCEEDED(hr)) {
  wprintf(L"Create ret failed with 0x%x\n", hr);
  return FALSE;
 }
 //
 // Get the IADsTSUser interface from the user object.
 //
 hr = pNewObject-&gt;QueryInterface(IID_IADsTSUserEx, (void**)&amp;pTSUser);

 if( !SUCCEEDED(hr)) { 
  wprintf(L"QueryInterface for IADsTSUserEx failed with ret 0x%x\n",
          hr);
  return FALSE;
 }
 //
 // Get the IADsTSUser interface from the user object.
 //
 hr = pNewObject-&gt;QueryInterface(IID_IADsUser, (void**)&amp;pUser);

 if( !SUCCEEDED(hr)) {
  wprintf(L"QueryInterface for IAsUser failed with 0x%x\n", hr);
  return FALSE;
 }
 pNewObject-&gt;Release();

 //
 // Set TerminalServicesProfilePath
 //
 pTSUser-&gt;put_TerminalServicesProfilePath(L"c:\\windows");
 pTSUser-&gt;Release();

 //
 // Commit the object data to the directory.
 //
 pUser-&gt;SetInfo();
 pUser-&gt;Release();
 CoUninitialize();
</pre>
</td>
</tr>
</table></span></div>
You can use the following script examples to bind to a provider's namespace. Two examples bind with supplied 
     credentials; two bind without credentials.

The first example shows a script that binds to the Security Accounts Manager (SAM) database with the 
      supplied credentials.

The second example shows a script that binds to the Active Directory database with the supplied 
     credentials.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Set DSO = GetObject("WinNT:")
Set usr = DSO.OpenDSObject(
    "WinNT://Server1/Test,user",
    Domain\User,
    Password,
    ADS_SECURE_AUTHENTICATION)
Wscript.echo usr.TerminalServicesProfilePath
usr.TerminalServicesProfilePath = "profile path"
usr.SetInfo
WScript.echo usr.TerminalServicesProfilePath
</pre>
</td>
</tr>
</table></span><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Set DSO = GetObject("LDAP:")
Set usr = DSO.OpenDSObject(
    "LDAP://DOMAIN/CN=Test,CN=Users,DC=Server1,DC=Domain,DC=com",
    Domain\User,
    Password,
    ADS_SECURE_AUTHENTICATION)
Wscript.echo usr.TerminalServicesProfilePath
usr.TerminalServicesProfilePath = "profile path"
usr.SetInfo
WScript.echo usr.TerminalServicesProfilePath
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7af8fe94-15db-49dc-ba4a-b79601205f59">IADsTSUserEx</a>
 

 

