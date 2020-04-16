---
UID: NN:iads.IADsAcl
title: IADsAcl (iads.h)
description: The IADsAcl interface provides methods for an ADSI client to access and manipulate the ACL or Inherited ACL attribute values. This interface manipulates the attributes.helpviewer_keywords: ["IADsAcl","IADsAcl interface [ADSI]","IADsAcl interface [ADSI]","described","_ds_iadsacl","adsi.iadsacl","iads/IADsAcl"]
old-location: adsi\iadsacl.htm
tech.root: adsi
ms.assetid: 71aebf28-f906-4a86-8bdb-ecb0626a350f
ms.date: 12/05/2018
ms.keywords: IADsAcl, IADsAcl interface [ADSI], IADsAcl interface [ADSI],described, _ds_iadsacl, adsi.iadsacl, iads/IADsAcl
f1_keywords:
- iads/IADsAcl
dev_langs:
- c++
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
- IADsAcl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsAcl interface


## -description


The <b>IADsAcl</b> interface provides methods for an ADSI client to access and manipulate the <b>ACL</b> or <b>Inherited ACL</b> attribute values. This interface manipulates the attributes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsAcl</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsAcl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsAcl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsacl-copyacl">CopyAcl</a>
</td>
<td align="left" width="63%">
Creates a new copy of the ACL.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsAcl</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsacl-property-methods">Privileges</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets and sets the privilege setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsacl-property-methods">ProtectedAttrName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets and sets the name of a protected attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsacl-property-methods">SubjectName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets and sets the name of a subject.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsacl-property-methods">IADsAcl Property Methods</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

