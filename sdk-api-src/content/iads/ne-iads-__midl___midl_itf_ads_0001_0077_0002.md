---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0077_0002
title: "__MIDL___MIDL_itf_ads_0001_0077_0002"
author: windows-sdk-content
description: Specifies the available options for examining security data of an object.
old-location: adsi\ads_security_info_enum.htm
old-project: ADSI
ms.assetid: 9cd1bb86-313d-4499-97ae-0b53a13a804b
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ADS_SECURITY_INFO_DACL, ADS_SECURITY_INFO_ENUM, ADS_SECURITY_INFO_ENUM enumeration [ADSI], ADS_SECURITY_INFO_GROUP, ADS_SECURITY_INFO_OWNER, ADS_SECURITY_INFO_SACL, __MIDL___MIDL_itf_ads_0001_0077_0002, _ds_ads_security_info_enum, adsi.ads__security__info__enum, adsi.ads_security_info_enum, iads/ADS_SECURITY_INFO_DACL, iads/ADS_SECURITY_INFO_ENUM, iads/ADS_SECURITY_INFO_GROUP, iads/ADS_SECURITY_INFO_OWNER, iads/ADS_SECURITY_INFO_SACL
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
req.idl: IAccess.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ADS_SECURITY_INFO_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_SECURITY_INFO_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

