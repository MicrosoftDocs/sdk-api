---
UID: NN:iads.IADsAcl
title: IADsAcl
author: windows-sdk-content
description: The IADsAcl interface provides methods for an ADSI client to access and manipulate the ACL or Inherited ACL attribute values. This interface manipulates the attributes.
old-location: adsi\iadsacl.htm
old-project: ADSI
ms.assetid: 71aebf28-f906-4a86-8bdb-ecb0626a350f
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IADsAcl, IADsAcl interface [ADSI], IADsAcl interface [ADSI],described, _ds_iadsacl, adsi.iadsacl, iads/IADsAcl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Activeds.dll
api_name:
-	IADsAcl
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsAcl interface


## -description


The <b>IADsAcl</b> interface provides methods for an ADSI client to access and manipulate the <b>ACL</b> or <b>Inherited ACL</b> attribute values. This interface manipulates the attributes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsAcl</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IADsAcl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/9ed78d7d-3448-4a49-920f-97221584541c">CopyAcl</a>
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

<a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">Privileges</a>


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

<a href="https://msdn.microsoft.com/eb4786d7-d366-4924-8255-dc28ea47a246">ProtectedAttrName</a>


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

<a href="https://msdn.microsoft.com/eb4786d7-d366-4924-8255-dc28ea47a246">SubjectName</a>


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




<a href="https://msdn.microsoft.com/eb4786d7-d366-4924-8255-dc28ea47a246">IADsAcl Property Methods</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

