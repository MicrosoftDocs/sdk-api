---
UID: NN:iads.IADsSecurityUtility
title: IADsSecurityUtility
author: windows-sdk-content
description: The IADsSecurityUtility interface is used to get, set, or retrieve the security descriptor on a file, fileshare, or registry key.
old-location: adsi\iadssecurityutility.htm
tech.root: ADSI
ms.assetid: 781eda1e-1f13-4bb4-ae8e-c9bf4c08e125
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IADsSecurityUtility, IADsSecurityUtility interface [ADSI], IADsSecurityUtility interface [ADSI],described, _ds_iadssecurityutility, adsi.iadssecurityutility, iads/IADsSecurityUtility
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
 - IADsSecurityUtility
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsSecurityUtility interface


## -description


The <b>IADsSecurityUtility</b> interface is used to get, set, or retrieve the security descriptor on a file, fileshare, or registry key. You can also use it to convert the security descriptor to or from raw or hexadecimal mode and you can limit the scope of the security descriptor data retrieved or set by indicating whether you want it for the owner, group, DACL, or SACL.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsSecurityUtility</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IADsSecurityUtility</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsSecurityUtility</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea6509bd-5625-458b-be7a-abb43ba2f46e">ConvertSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Converts a security descriptor from one format to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95f4fbd9-03f8-4f2f-9314-e628186e51a4">GetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves a security descriptor for the specified file, fileshare, or registry key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0f5c1fb-14fa-4d84-aa82-0d5e24ec5c2b">SetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Sets the security descriptor for the specified file, file share, or registry key.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsSecurityUtility</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b54ebe68-f7ce-484e-9378-04662b7a1051">SecurityMask</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Determines which elements of the security descriptor to retrieve or set.

</td>
</tr>
</table> 


## -remarks



To read the system access-control list (SACL) of a file or directory, the <b>SE_SECURITY_NAME</b> privilege must be enabled for the calling process. For more information about retrieving the SACL for an object, see <a href="https://msdn.microsoft.com/b1da91a2-d9b0-48a3-9de5-1e588209032d">Retrieving an Object's SACL</a>.

For more information and a code example that shows how to use the <b>IADsSecurityUtility</b> interface to add an ACE to a file, see <a href="https://msdn.microsoft.com/d47d3ebe-cc14-412d-be27-841e25b43c3a">Example Code for Adding an ACE to a File</a>.




## -see-also




<a href="https://msdn.microsoft.com/3ae0ec98-9184-4ab3-b859-39c0d677eb0d">ADS_PATHTYPE_ENUM</a>



<a href="https://msdn.microsoft.com/503247b6-3119-4514-9831-c8f0ef50c0fa">ADS_SD_FORMAT_ENUM</a>



<a href="https://msdn.microsoft.com/d47d3ebe-cc14-412d-be27-841e25b43c3a">Example Code for Adding an ACE to a File</a>



<a href="https://msdn.microsoft.com/6d2cd45b-0dc6-4bb3-9c41-014bec71f258">IADsAccessControlEntry</a>



<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/de92d9cc-bc9d-4dc5-aa79-01f4d3050c35">IAccessControlList</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/7233a82f-fc38-4718-b674-4e6a00666184">Security Descriptors on Files and Registry Keys</a>



<a href="https://msdn.microsoft.com/1434f0ec-a87b-4b75-9013-a1ca27956ec4">Security Interfaces</a>
 

 

