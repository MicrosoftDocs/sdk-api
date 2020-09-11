---
UID: NN:iads.IADsADSystemInfo
title: IADsADSystemInfo (iads.h)
description: The IADsADSystemInfo interface retrieves data about the local computer if it is running a Windows operating system in a Windows domain. For example, you can get the domain, site, and distinguished name of the local computer.
helpviewer_keywords: ["ADSystemInfo","IADsADSystemInfo","IADsADSystemInfo interface [ADSI]","IADsADSystemInfo interface [ADSI]","described","_ds_iadsadsysteminfo","adsi.iadsadsysteminfo","iads/IADsADSystemInfo"]
old-location: adsi\iadsadsysteminfo.htm
tech.root: adsi
ms.assetid: 5573d37b-10a8-4176-80c7-711552ff36cb
ms.date: 12/05/2018
ms.keywords: ADSystemInfo, IADsADSystemInfo, IADsADSystemInfo interface [ADSI], IADsADSystemInfo interface [ADSI],described, _ds_iadsadsysteminfo, adsi.iadsadsysteminfo, iads/IADsADSystemInfo
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
 - IADsADSystemInfo
 - iads/IADsADSystemInfo
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
 - IADsADSystemInfo
 - ADSystemInfo
---

# IADsADSystemInfo interface


## -description

The <b>IADsADSystemInfo</b> interface retrieves data about the local computer if it is running a Windows operating system in a Windows domain. For example, you can get the domain, site, and distinguished name of the local computer.

The <b>IADsADSystemInfo</b> interface is implemented on the <b>ADSystemInfo</b> object residing in adsldp.dll, which is included with the standard installation of ADSI on Windows 2000. You must explicitly create an instance of the <b>ADSystemInfo</b> object in order to call the methods on the <b>IADsADSystemInfo</b> interface. This requirement amounts to creating an <b>ADSystemInfo</b> instance with the  <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function in C/C++.

```cpp
IADsADSystemInfo *pADsys;
HRESULT hr = CoCreateInstance(CLSID_ADSystemInfo,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IADsADSystemInfo,
                              (void**)&pADsys);
```

You can also use the <b>New</b> operator in Visual Basic.

```vb
Dim adSys as New ADSystemInfo
```

Or you can call the <b>CreateObject</b> function in a scripting environment, supplying "ADSystemInfo" as the ProgID.

```vb
Dim adSys
Set adSys = CreateObject("ADSystemInfo")
```

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsADSystemInfo</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsADSystemInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsADSystemInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsadsysteminfo-getanydcname">GetAnyDCName</a>
</td>
<td align="left" width="63%">
Retrieves the DNS name of a domain controller in the local computer domain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsadsysteminfo-getdcsitename">GetDCSiteName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the local computer site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsadsysteminfo-gettrees">GetTrees</a>
</td>
<td align="left" width="63%">
Retrieves the DNS names of all the directory trees in the local computer forest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsadsysteminfo-refreshschemacache">RefreshSchemaCache</a>
</td>
<td align="left" width="63%">
Refreshes the ADSI Active Directory schema cache on the local computer.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsADSystemInfo</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsadsysteminfo-property-methods">ComputerName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the distinguished name of the local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsadsysteminfo-property-methods">DomainDNSName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the DNS name of the local computer domain, for example "example.fabrikam.com".

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsadsysteminfo-property-methods">DomainShortName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the short name of the local computer domain, for example "myDom".

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsadsysteminfo-property-methods">ForestDNSName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the DNS name of the local computer forest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsadsysteminfo-property-methods">IsNativeMode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Determines whether the local computer domain is in native or mixed mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsadsysteminfo-property-methods">PDCRoleOwner</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the distinguished name of the NTDS-DSA object for the DC that owns the primary domain controller role in the local computer domain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsadsysteminfo-property-methods">SchemaRoleOwner</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the distinguished name of the NTDS-DSA object for the DC that owns the schema role in the local computer forest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsadsysteminfo-property-methods">SiteName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the site name of the local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsadsysteminfo-property-methods">UserName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the Active Directory distinguished name of the current user, which is the logged-on user or the user impersonated by the calling thread.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsadsysteminfo-property-methods">IADsADSystemInfo Property Methods</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>

