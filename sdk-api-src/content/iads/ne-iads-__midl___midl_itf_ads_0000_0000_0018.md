---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0018
title: "__MIDL___MIDL_itf_ads_0000_0000_0018"
author: windows-sdk-content
description: Specifies authentication options used in ADSI for binding to directory service objects.
old-location: adsi\ads_authentication_enum.htm
tech.root: ADSI
ms.assetid: 3a45e0c2-5392-456d-80c9-ebd17d056a85
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ADS_AUTHENTICATION_ENUM, ADS_AUTHENTICATION_ENUM enumeration [ADSI], ADS_AUTH_RESERVED, ADS_FAST_BIND, ADS_NO_AUTHENTICATION, ADS_NO_REFERRAL_CHASING, ADS_PROMPT_CREDENTIALS, ADS_READONLY_SERVER, ADS_SECURE_AUTHENTICATION, ADS_SERVER_BIND, ADS_USE_DELEGATION, ADS_USE_ENCRYPTION, ADS_USE_SEALING, ADS_USE_SIGNING, ADS_USE_SSL, __MIDL___MIDL_itf_ads_0000_0000_0018, _ds_ads_authentication_enum, adsi.ads__authentication__enum, adsi.ads_authentication_enum, iads/ADS_AUTHENTICATION_ENUM, iads/ADS_AUTH_RESERVED, iads/ADS_FAST_BIND, iads/ADS_NO_AUTHENTICATION, iads/ADS_NO_REFERRAL_CHASING, iads/ADS_PROMPT_CREDENTIALS, iads/ADS_READONLY_SERVER, iads/ADS_SECURE_AUTHENTICATION, iads/ADS_SERVER_BIND, iads/ADS_USE_DELEGATION, iads/ADS_USE_ENCRYPTION, iads/ADS_USE_SEALING, iads/ADS_USE_SIGNING, iads/ADS_USE_SSL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_AUTHENTICATION_ENUM
product: Windows
targetos: Windows
req.typenames: ADS_AUTHENTICATION_ENUM
req.redist: 
---

# __MIDL___MIDL_itf_ads_0000_0000_0018 enumeration


## -description


The <b>ADS_AUTHENTICATION_ENUM</b> enumeration 
   specifies authentication options used in ADSI for binding to directory service objects. When 
   calling <a href="https://msdn.microsoft.com/9daf6f91-6c58-46a8-ba05-149f28b53829">IADsOpenDSObject</a> or 
   <a href="https://msdn.microsoft.com/c4b85d8e-b33b-47a4-b7d7-5f901f80dce9">ADsOpenObject</a> to bind to an ADSI object, provide at least 
   one of the options. In general, different providers will have different implementations. The options documented 
   here apply to the providers supplied by Microsoft included with the ADSI SDK. For more information, see 
   <a href="https://msdn.microsoft.com/419d7953-a879-4d6c-be74-173d76c3f932">ADSI System Providers</a>.


## -enum-fields




### -field ADS_SECURE_AUTHENTICATION

Requests secure authentication. When this flag is set, the WinNT provider uses NT LAN Manager (NTLM) to 
      authenticate the client. Active Directory will use Kerberos, and possibly NTLM, to authenticate the client. When 
      the user name and password are <b>NULL</b>, ADSI binds to the object using the security 
      context of the calling thread, which is either the security context of the user account under which the 
      application is running or of the client user account that the calling thread represents.


### -field ADS_USE_ENCRYPTION

Requires ADSI to use encryption for data exchange over the network.

<div class="alert"><b>Note</b>  This option is not supported by the WinNT provider.</div>
<div> </div>

### -field ADS_USE_SSL

The channel is encrypted using Secure Sockets Layer (SSL). Active Directory requires that the Certificate 
       Server be installed to support SSL.

If this flag is not combined with the <b>ADS_SECURE_AUTHENTICATION</b> flag and the 
       supplied credentials are <b>NULL</b>, the bind will be performed anonymously. If this flag 
       is combined with the <b>ADS_SECURE_AUTHENTICATION</b> flag and the supplied credentials are 
       <b>NULL</b>, then the credentials of the calling thread are used.

<div class="alert"><b>Note</b>  This option is not supported by the WinNT provider.</div>
<div> </div>

### -field ADS_READONLY_SERVER

A writable domain controller is not required. If your application only reads or queries data from Active 
       Directory, you should use this flag to open the sessions. This allows the application to take advantage of 
       Read-Only DCs (RODCs).

In Windows Server 2008, ADSI attempts to connect to either Read-Only DCs (RODCs) or writable DCs. This 
       allows the use of an RODC for the access and enables the application to run in a branch or perimeter network 
       (also known as DMZ, demilitarized zone, and screened subnet), without the need for direct connectivity with a 
       writable DC.

For more information about programming for RODC compatibility, see the 
       <a href="http://go.microsoft.com/fwlink/p/?linkid=217948">Read-Only Domain Controllers Application Compatibility Guide</a>.


### -field ADS_PROMPT_CREDENTIALS

This flag is not supported.


### -field ADS_NO_AUTHENTICATION

Request no authentication. The providers may attempt to bind the client, as an anonymous user, to the 
      target object. The WinNT provider does not support this flag. Active Directory establishes a connection between 
      the client and the targeted object, but will not perform authentication. Setting this flag amounts to requesting 
      an anonymous binding, which indicates all users as the security context.


### -field ADS_FAST_BIND

When this flag is set, ADSI will not attempt to query the <b>objectClass</b> 
       property and thus will only expose the base interfaces supported by all ADSI objects instead of the full object 
       support. A user can use this option to increase the performance in a series of object manipulations that involve 
       only methods of the base interfaces. However, ADSI will not verify that any of the requested objects actually 
       exist on the server. For more information, see 
       <a href="https://msdn.microsoft.com/cf41b0c4-7459-49cf-945b-8462c7d19947">Fast Binding Options for Batch Write/Modify Operations</a>.

This option is also useful for binding to non-Active Directory directory services, for example Exchange 5.5, 
       where the <b>objectClass</b> query would fail.


### -field ADS_USE_SIGNING

Verifies data integrity. The <b>ADS_SECURE_AUTHENTICATION</b> flag must also be set also 
       to use signing.

<div class="alert"><b>Note</b>  This option is not supported by the WinNT provider.</div>
<div> </div>

### -field ADS_USE_SEALING

Encrypts data using Kerberos. The <b>ADS_SECURE_AUTHENTICATION</b> flag must also be set 
       to use sealing.

<div class="alert"><b>Note</b>  This option is not supported by the WinNT provider.</div>
<div> </div>

### -field ADS_USE_DELEGATION

Enables ADSI to delegate the user security context, which is necessary for moving objects across domains.


### -field ADS_SERVER_BIND

If an Active Directory DNS server name is passed in the LDAP path, this forces an A-record lookup and 
       bypasses any SRV record lookup when resolving the host name.

<div class="alert"><b>Note</b>  This option is not supported by the WinNT provider.</div>
<div> </div>

### -field ADS_NO_REFERRAL_CHASING

Specify this flag to turn referral chasing off for the life of the connection. However, even when this flag 
       is specified, ADSI still allows the setting of referral chasing behavior for container enumeration when set 
       using <b>ADS_OPTION_REFERRALS</b> in 
       <a href="https://msdn.microsoft.com/afb32e03-7e4e-4df9-87c7-db962d62e5f0">ADS_OPTION_ENUM</a> (as documented in container enumeration 
       with referral chasing in 
       <a href="https://msdn.microsoft.com/e6e43c99-fc8b-4f34-82cf-8cf30c506859">IADsObjectOptions::SetOption</a>) and 
       searching separately (as documented in 
       <a href="https://msdn.microsoft.com/ef97eafd-5227-4dd7-9f8a-6b4591261f79">Referral Chasing with IDirectorySearch</a>).

<div class="alert"><b>Note</b>  This option is not supported by the WinNT provider.</div>
<div> </div>

### -field ADS_AUTH_RESERVED

Reserved.


## -remarks



The <b>ADS_SECURE_AUTHENTICATION</b> flag can be used in combination with other flags such 
    as <b>ADS_READONLY_SERVER</b>, <b>ADS_PROMPT_CREDENTIALS</b>, 
    <b>ADS_FAST_BIND</b>, and so on.

Serverless binding refers to a process in which a client attempts to bind to an Active Directory object 
    without explicitly specifying an Active Directory server in the binding string. This is possible because the LDAP 
    provider relies on the locator services of Windows to find the best domain controller (DC) for the client. 
    However, the client must have an account on the Active Directory domain controller to take advantage of the 
    serverless binding feature, and the DC used by a serverless bind will always be located in the default domain; 
    that is, the domain associated with the current security context of the thread that performs the binding.

Because VBScript cannot read data from a type library, VBScript applications do not recognize the symbolic 
    constants as defined above. Use the numerical constants instead to set the appropriate flags in your VBScript 
    applications. To use the symbolic constants as a good programming practice, write explicit declarations of such 
    constants, as done here, in your Visual Basic Scripting edition application.


#### Examples

The following code example shows how to use 
     <a href="https://msdn.microsoft.com/9daf6f91-6c58-46a8-ba05-149f28b53829">IADsOpenDSObject</a> to open an object on fabrikam with 
     secure authentication for the WinNT provider.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Const ADS_SECURE_AUTHENTICATION = 1

Dim dso As IADsOpenDSObject
Dim domain As IADsDomain
 
Set dso = GetObject("WinNT:")
Set domain = dso.OpenDSObject("WinNT://Fabrikam", vbNullString, vbNullString, ADS_SECURE_AUTHENTICATION)</pre>
</td>
</tr>
</table></span></div>
The following code example shows how the <b>ADS_SECURE_AUTHENTICATION</b> flag is used 
     with <a href="https://msdn.microsoft.com/c4b85d8e-b33b-47a4-b7d7-5f901f80dce9">ADsOpenObject</a> for validating the user bound as 
     "JeffSmith". The user name can be of the UPN format: "JeffSmith@Fabrikam.com", as well as the distinguished name 
     format: "CN=JeffSmith,DC=Fabrikam,DC=COM".

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADs *pObject = NULL;
HRESULT hr;
hr = ADsOpenObject(_bstr_t("LDAP://CN=JeffSmith, DC=fabrikam, DC=com"),
                   NULL,
                   NULL,
                   ADS_SECURE_AUTHENTICATION, 
                   IID_IADs,
                   (void**) &amp;pObject);
if (hr != S_OK)
    {} // Handle open object errors here.
else
    {} // Object was retrieved, continue processing here.</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>



<a href="https://msdn.microsoft.com/419d7953-a879-4d6c-be74-173d76c3f932">ADSI System Providers</a>



<a href="https://msdn.microsoft.com/c4b85d8e-b33b-47a4-b7d7-5f901f80dce9">ADsOpenObject</a>



<a href="https://msdn.microsoft.com/6d2cd45b-0dc6-4bb3-9c41-014bec71f258">IADsAccessControlEntry</a>



<a href="https://msdn.microsoft.com/9daf6f91-6c58-46a8-ba05-149f28b53829">IADsOpenDSObject</a>
 

 

