---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL___MIDL_itf_ads_0001_0077_0002 enumeration


## -description


The <b>ADS_SECURITY_INFO_ENUM</b> enumeration specifies the available options for examining security data of an object.


## -enum-fields




### -field ADS_SECURITY_INFO_OWNER

Reads or sets the owner data.


### -field ADS_SECURITY_INFO_GROUP

Reads or sets the group data.


### -field ADS_SECURITY_INFO_DACL

Reads or sets the discretionary access-control list data.


### -field ADS_SECURITY_INFO_SACL

Reads or sets the system access-control list data.


## -remarks



The options defined in this enumeration are bit-masks. More than one option can be set using appropriate bitwise operations.

To read the security data for an object, use the  <a href="https://msdn.microsoft.com/1884efe5-86f5-4579-a25e-2ff9c9a6ec2a">IADsObjectOptions</a> interface, supplying the security data options listed in this enumeration.

The following list lists common flag combinations and their use.

<table>
<tr>
<th>Flag combination</th>
<th>Description</th>
</tr>
<tr>
<td><b>ADS_SECURITY_INFO_OWNER</b>, <b>ADS_SECURITY_INFO_GROUP</b>, and <b>ADS_SECURITY_INFO_DACL</b></td>
<td>Enable users to read the security data of the owner, group, or DACL of an object. This is the default setting when an object is created.</td>
</tr>
<tr>
<td><b>ADS_SECURITY_INFO_OWNER</b>, <b>ADS_SECURITY_INFO_GROUP</b>, <b>ADS_SECURITY_INFO_DACL</b>, and <b>ADS_SECURITY_INFO_SACL</b></td>
<td>Enable users to read the SACL. The <b>ADS_SECURITY_INFO_SACL</b> flag cannot be used by itself.</td>
</tr>
</table>
 

Presently, such options are available for Active Directory only.

Because Visual Basic Scripting Edition (VBScript) cannot read data from a type library, an application must use the appropriate numeric constants, instead of the symbolic constants, to set the appropriate flags. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here.


#### Examples

The following code example displays the number of access control entries in a SACL.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Const ADS_SECURITY_INFO_OWNER = &amp;H1
Const ADS_SECURITY_INFO_GROUP = &amp;H2
Const ADS_SECURITY_INFO_DACL = &amp;H4
Const ADS_SECURITY_INFO_SACL = &amp;H8

Const ADS_OPTION_SECURITY_MASK = 3

Dim x As IADs
Dim dso As IADsOpenDSObject
Dim adsPath As String
Dim sd As IADsSecurityDescriptor
Dim sacl As IADsAccessControlList
Dim objOps As IADsObjectOptions
Dim opt As Variant
Dim canReadSacl As Variant
 
Set dso = GetObject("LDAP:")
adsPath = "LDAP://ArcSrv1/dc=Sales,dc=Fabrikam,dc=com"
Set x = dso.OpenDSObject(adsPath, vbNullString, vbNullString, 1)
Set objOps = x
 
canReadSacl = ADS_SECURITY_INFO_OWNER _
                Or ADS_SECURITY_INFO_GROUP _
                Or ADS_SECURITY_INFO_DACL _
                Or ADS_SECURITY_INFO_SACL
 
opt = objOps.GetOption(ADS_OPTION_SECURITY_MASK)
If opt &lt;&gt; canReadSacl Then
    objOps.SetOption ADS_OPTION_SECURITY_MASK, canReadSacl
End If
Set sd = x.Get("ntSecurityDescriptor")
Set sacl = sd.SystemAcl
Debug.Print "sacl(aceCount)= " &amp; sacl.AceCount</pre>
</td>
</tr>
</table></span></div>
The following code example displays the number of access-control entries in a system ACL. For brevity, error checking is omitted.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void TestObjectOptions()
{
    long lCanReadSACL = ADS_SECURITY_INFO_OWNER | 
        ADS_SECURITY_INFO_GROUP | 
        ADS_SECURITY_INFO_DACL | 
        ADS_SECURITY_INFO_SACL;

    HRESULT hr = S_OK;
    CComPtr&lt;IADs&gt; spObj;
    hr = ADsOpenObject(L"LDAP://arcSrv1/dc=Sales,dc=Fabrikam,dc=com", 
        NULL, 
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADs,
        (void**)&amp;spObj);
    if(S_OK != hr)
    {
        return;
    }

    CComPtr&lt;IADsObjectOptions&gt; spObjOps;
    hr = spObj-&gt;QueryInterface(IID_IADsObjectOptions, (void**)&amp;spObjOps);
    if(S_OK != hr)
    {
        return;
    }

    CComVariant svar;
    hr = spObjOps-&gt;GetOption(ADS_OPTION_SECURITY_MASK, &amp;svar);
    if(S_OK != hr)
    {
        return;
    }

    if(V_I4(&amp;svar) != lCanReadSACL)
    {
        svar = lCanReadSACL;
        hr = spObjOps-&gt;SetOption(ADS_OPTION_SECURITY_MASK, svar);
    }

    hr = spObj-&gt;Get(CComBSTR("ntSecurityDescriptor"), &amp;svar);
    if(S_OK != hr)
    {
        return;
    }

    CComPtr&lt;IADsSecurityDescriptor&gt; spSd;
    hr = V_DISPATCH(&amp;svar)-&gt;QueryInterface(IID_IADsSecurityDescriptor, 
                                            (void**)&amp;spSd);
    if(S_OK != hr)
    {
        return;
    }

    CComPtr&lt;IDispatch&gt; spDisp;
    hr = spSd-&gt;get_SystemAcl(&amp;spDisp);
    if(S_OK != hr)
    {
        return;
    }

    CComPtr&lt;IADsAccessControlList&gt; spSacl;
    hr = spDisp-&gt;QueryInterface(IID_IADsAccessControlList, 
                                (void**)&amp;spSacl);
    if(S_OK != hr)
    {
        return;
    }

    LONG lOptions;
    hr = spSacl-&gt;get_AceCount(&amp;lOptions);
    if(S_OK != hr)
    {
        return;
    }

    _tprintf(TEXT("Number of ACE's in the SACL is %d\n"), lOptions);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>



<a href="https://msdn.microsoft.com/1884efe5-86f5-4579-a25e-2ff9c9a6ec2a">IADsObjectOptions</a>



<a href="https://msdn.microsoft.com/77a994d2-81ae-4afb-be5c-be8d7159a2c2">IADsObjectOptions::GetOption</a>



<a href="https://msdn.microsoft.com/e6e43c99-fc8b-4f34-82cf-8cf30c506859">IADsObjectOptions::SetOption</a>
 

 

